# How to load resource from the resources folder?

```java
@Autowired
	ResourceLoader resourceLoader;
```


```java
		File file = resourceLoader.getResource("sample_data/Test/Invoice_6.pdf").getFile();
		log.info("filename : {}", file.getName());
```

