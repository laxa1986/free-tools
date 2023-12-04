What do you do when you feel pain? You might get some pain killer, but if pain comes back - you'd likely gonna see a doctor.
Same with logs - if you see errors or warnings - you will likely take some action to fix them. Unless you logs are somewhat
you do not want to look at! So idea is to make nice and need local logging, so that it is easy to read and spot any badness

This log pattern:
- removes date (you only need time for local run)
- keeps very small space for thread name - it is rare to need to know full thread name when run locally
- makes log level colorful: WARN is orange and ERROR is red - so it is easy to spot them

Most of the time your log record fits one line, so you can clearly see it and do not need a line wrap

```
10:15:17.034 INFO   main database.base.BaseDatabaseType - Database: jdbc:postgresql://localhost:5432/test (PostgreSQL 15.4)
10:15:17.069 INFO   main re.internal.command.DbValidate - Successfully validated 1 migration (execution time 00:00.012s)
10:15:17.095 INFO   main ore.internal.command.DbMigrate - Current version of schema "public": 1
10:15:17.096 INFO   main ore.internal.command.DbMigrate - Schema "public" is up to date. No migration necessary.
10:15:17.134 INFO   main te.jpa.internal.util.LogHelper - HHH000204: Processing PersistenceUnitInfo [name: default]
10:15:17.152 INFO   main org.hibernate.Version          - HHH000412: Hibernate ORM core version 6.2.13.Final
10:15:17.153 INFO   main org.hibernate.cfg.Environment  - HHH000406: Using bytecode reflection optimizer
10:15:17.250 INFO   main .j.p.SpringPersistenceUnitInfo - No LoadTimeWeaver setup: ignoring JPA class transformer
10:15:17.594 INFO   main e.t.j.p.i.JtaPlatformInitiator - HHH000489: No JTA platform available (set 'hibernate.transaction.jta.platform' to enable JTA platform integration)
10:15:17.594 INFO   main tainerEntityManagerFactoryBean - Initialized JPA EntityManagerFactory for persistence unit 'default'
10:15:17.815 INFO   main oyote.http11.Http11NioProtocol - Starting ProtocolHandler ["http-nio-80"]
10:15:17.825 INFO   main mbedded.tomcat.TomcatWebServer - Tomcat started on port(s): 80 (http) with context path ''
10:15:17.829 INFO   main com.agilecustoms.Application   - Started Application in 1.667 seconds (process running for 1.815)
```