<p>Some time we need us our own custom id generator strategy.
        For Custom Id generation we need to implement IdentifierGenerator interface and need to provide the body of *generate* method.

        If you will check the CustomIdGenerator class, it implement the  IdentifierGenerator interface.
        and you can use your custom generator like </p>
`@Id
@GeneratedValue(generator = "name of GenericGenerator")
@GenericGenerator(name = "any custom name",
        strategy = "class with package name")
private String id;`
