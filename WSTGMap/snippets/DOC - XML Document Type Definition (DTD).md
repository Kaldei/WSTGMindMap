#xml 

## Document Type Definition (DTD) 
The XML Document Type Definition contains declarations that can define the structure of an XML document, the types of data values it can contain, and other items. The DTD is declared within the optional `DOCTYPE` element at the start of the XML document.

The DTD can be fully self-contained within the document itself (known as an "internal DTD") or can be loaded from elsewhere (known as an "external DTD") or can be hybrid of the two. 


## XML Custom Entities
XML allows custom entities to be defined within the DTD.


## XML External Entities (XXE)
 XML external entities are a type of custom entity whose definition is located outside of the DTD where they are declared.
 The declaration of an external entity uses the `SYSTEM` keyword and must specify a URL from which the value of the entity should be loaded.