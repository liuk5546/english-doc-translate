## Java, JDBC 和 mysql的类型
事实上，虽然会有四舍五入（round-off），溢出，精度缺损的出现，任意数据类型都可以被转换成`java.lang.String`，任意数字类型可以被转换成java的数字类型（numeric types, 比如int float）。  
| mysql类型                            | GetColumnClassNam的返回类型 | GetCloumnClassName的返回类型                                                                                                                                   |
|------------------------------------|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| BIT\(1\) \(new in MySQL\-5\.0\)    | BIT                    | java\.lang\.Boolean                                                                                                                                       |
| BIT\( > 1\) \(new in MySQL\-5\.0\) | BIT                    | byte\[\]                                                                                                                                                  |
| TINYINT                            | TINYINT                | java\.lang\.Boolean if the configuration property tinyInt1isBit is set to true \(the default\) and the storage size is 1, or java\.lang\.Integer if not\. |
| BOOL, BOOLEAN                      | TINYINT	               | See TINYINT, above as these are aliases for TINYINT\(1\), currently\.                                                                                     |
