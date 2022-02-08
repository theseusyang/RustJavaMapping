# JavaC++RustMapping
Rust<->Java<->C++ 语法对照表

### shot 数据类型

|  Java   | Rust  |
|  ----  | ----  |
| shot  | i16 |

Java: </p>
<code>
void onMemoryReserved(MemoryPool memoryPool, short target);
</code>

Rust: </p>
<code>
fn onMemoryReserved(memoryPool: MemoryPool, target: i16);
</code>

### double 数据类型

|  Java   | Rust  |
|  ----  | ----  |
| double  | f64 |


Java: </p>
<code>
void onMemoryReserved(MemoryPool memoryPool, double target);
</code>

Rust: </p>
<code>
fn onMemoryReserved(memoryPool: MemoryPool, target: f64);
</code>


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


### foreach

|  Java   | Rust  |
|  ----  | ----  |
| for  | foreach |

Java: </p>
<code>
listeners.forEach(listener -> listener.onMemoryReserved(this, MppConfig.getInstance().getMemoryRevokingTarget()));
</code>

Rust</p>
<code>
  for listener in listeners.iter(){ listener.onMemoryReserved(&self, MppConfig::getInstance()::getMemoryRevokingTarget())};
</code>

C++: </p>
<code>
for (auto it = snapshot_files.rbegin(); it != snapshot_files.rend(); ++it) 
</code>

Rust</p>
<code>
  ...
</code>


### HashMap

|  Java   | Rust  |
|  ----  | ----  |
| HashMap  | HashMap |

Java: </p>
<code>
Map<String, MemoryStatisticsGroup> memoryStatistics = new HashMap();
</code>
  
Rust: </p>
<code> 
let mut memoryStatistics: HashMap<&str, MemoryStatisticsGroup> = HashMap::new();
</code>

### std::pair
|  C++   | Rust  |
|  ----  | ----  |
| std::pair  | cosmwasm_std::Pair |
  
C++: </p>
<code>
std::pair<query::Expression *, size_t>
</code>  

Rust: </p>
<code> 
pub type Pair<V = Vec<u8>> = (Vec<u8>, V);
</code>
