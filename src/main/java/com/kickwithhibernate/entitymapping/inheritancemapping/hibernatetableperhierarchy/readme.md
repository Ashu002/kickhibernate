By this inheritance strategy, we can map the whole hierarchy by single table only.

        In this example here we have 3 classes:
        Parent
        Child1
        Child2
        Child1 and Child2 extending Parent class, so in case of inheritance strategy 1 table will create in database with the name of parent class
and will hold column name id and all included fields of child classes,



                Initial SessionFactory creation failed.org.hibernate.MappingException: No discriminator found for com.kickwithhibernate.entitymapping.inheritancemapping.hibernatetableperhierarchy.withxml.Child2. Discriminator is needed when 'single-table-per-hierarchy' is used and a class has subclasses
        Exception in thread "main" java.lang.ExceptionInInitializerError
        at util.HibernateUtil.buildSessionFactory(HibernateUtil.java:20)
        at util.HibernateUtil.<clinit>(HibernateUtil.java:11)
        at com.kickwithhibernate.entitymapping.inheritancemapping.hibernatetableperhierarchy.withxml.TestHibernateTablePerHierarchy.createData(TestHibernateTablePerHierarchy.java:24)
        at com.kickwithhibernate.entitymapping.inheritancemapping.hibernatetableperhierarchy.withxml.TestHibernateTablePerHierarchy.main(TestHibernateTablePerHierarchy.java:12)
        Caused by: org.hibernate.MappingException: No discriminator found for com.kickwithhibernate.entitymapping.inheritancemapping.hibernatetableperhierarchy.withxml.Child2. Discriminator is needed when 'single-table-per-hierarchy' is used and a class has subclasses
        at org.hibernate.mapping.SingleTableSubclass.validate(SingleTableSubclass.java:62)
        at org.hibernate.cfg.Configuration.validate(Configuration.java:1360)
        at org.hibernate.cfg.Configuration.buildSessionFactory(Configuration.java:1851)
        at org.hibernate.cfg.Configuration.buildSessionFactory(Configuration.java:1930)
        at util.HibernateUtil.buildSessionFactory(HibernateUtil.java:15)
        ... 3 more
