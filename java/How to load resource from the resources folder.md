# How to load resource from the resources folder?

```java
@Autowired
ResourceLoader resourceLoader;
```


```java
File file = resourceLoader.getResource("sample_data/Test/Invoice_6.pdf").getFile();
log.info("filename : {}", file.getName());
```




```
➜  resources git:(master) ✗ tree 
.
|-- application.properties
`-- sample_data
    |-- Test
    |   |-- Invoice_6.pdf
    |   `-- Invoice_7.pdf
    `-- Train
        |-- Invoice_1.pdf
        |-- Invoice_2.pdf
        |-- Invoice_3.pdf
        |-- Invoice_4.pdf
        `-- Invoice_5.pdf
```
