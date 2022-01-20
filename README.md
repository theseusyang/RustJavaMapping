# RustJavaMapping
Rust&lt;->Java 语法对照表

### double 数据类型

|  Java   | Rust  |
|  ----  | ----  |
| double  | f64 |


Java: </p>
```void onMemoryReserved(MemoryPool memoryPool, double target);```

Rust: </p>
```fn onMemoryReserved(memoryPool: MemoryPool, target: f64);```


### Logger

|  Java   | Rust  |
|  ----  | ----  |
| Logger  | log |

Java: </p>
```private static final Logger logger = LoggerFactory.getLogger(A.class);```

Rust: </p>
```use log::{info, trace, warn};```

### UUID

|  Java   | Rust  |
|  ----  | ----  |
| UUID  | uuid |

Java: </p>
```final String poolName = UUID.randomUUID().toString();```

Rust: </p>
```let mut poolName: String = Uuid::new_v4();```



