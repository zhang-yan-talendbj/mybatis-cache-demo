# mybatis-cache-demo
gitchat-一步步学习mybatis缓存-演示代码


[聊聊MyBatis缓存机制](https://tech.meituan.com/2018/01/19/mybatis-cache.html)

                           
[mybatis configuration](https://mybatis.org/mybatis-3/configuration.html)

### localCacheScope:
MyBatis uses local cache to prevent circular references and speed up repeated nested queries. By default (SESSION) all queries executed during a session are cached. If localCacheScope=STATEMENT local session will be used just for statement execution, no data will be shared between two different calls to the same SqlSession.

```
<setting name="localCacheScope" value="STATEMENT"/>

mapper.StudentMapperTest.testLocalCache中的三个方法,会调用三次DB
```

