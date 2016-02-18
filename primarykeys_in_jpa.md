###Primary Keys in JPA


Create a sequence in oracle called DEMO_CUSTOMERS_SEQ
Notice that the generator name is the same as the name attribute in the @SequenceGenerator annotation below


@Id
@SequenceGenerator( name = "DemoCustomersSeq", sequenceName = "DEMO_CUSTOMERS_SEQ", allocationSize = 1, initialValue = 1 )
@GeneratedValue( strategy = GenerationType.SEQUENCE, generator = "DemoCustomersSeq" )