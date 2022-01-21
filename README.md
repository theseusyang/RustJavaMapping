# RustJavaMapping
Rust&lt;->Java 语法对照表

### double 数据类型

|  Java   | Rust  |
|  ----  | ----  |
| double  | f64 |


Java: </p>
<code>
```void onMemoryReserved(MemoryPool memoryPool, double target);```
</code>

Rust: </p>
```fn onMemoryReserved(memoryPool: MemoryPool, target: f64);```


### Logger

|  Java   | Rust  |
|  ----  | ----  |
| Logger  | log |

Java: </p>
<code>
```private static final Logger logger = LoggerFactory.getLogger(A.class);```</p>
```logger.info("The query use much more memory for the memory pool: " + name);```</p>
</code>

Rust: </p>
<code>
```use log::{info, trace, warn};```</p>
```info!("The query use much more memory for the memory pool: {}", name);```</p>
</code>



### UUID

|  Java   | Rust  |
|  ----  | ----  |
| UUID  | uuid |

Java: </p>
```final String poolName = UUID.randomUUID().toString();```

Rust: </p>
```let mut poolName: String = Uuid::new_v4();```



