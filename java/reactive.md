
# Reactive

## Backpressure: 

```java
Flux.just(1, 2, 3, 4)
  .log()
  .subscribe(new Subscriber<Integer>() {
    private Subscription s;
    int onNextAmount;
 
    @Override
    public void onSubscribe(Subscription s) {
        this.s = s;
        s.request(2);
    }
 
    @Override
    public void onNext(Integer integer) {
        elements.add(integer);
        onNextAmount++;
        if (onNextAmount % 2 == 0) {
            s.request(2);
        }
    }
 
    @Override
    public void onError(Throwable t) {}
 
    @Override
    public void onComplete() {}
});
```
