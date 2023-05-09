# Readings: Object-Oriented Programming, HTML Tables

## *Reading*

[Domain Modeling](https://github.com/codefellows/domain_modeling#domain-modeling)

### *Questions*

1. Explain why we need Domain Modeling.

### *Answers*

1. It allows a full conceptualization of a specific problem. The idea is to map out and articulate all data and behaviors of all entities involved within the problem domain.

___

[HTML Table Basics](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics)

### *Questions*

1. Why should tables not be used for page layouts?
2. List and describe 3 different semantic HTML elements used in an HTML `<table>`.

### *Answers*

1. Makes code harder to maintain and less accessible to any assistive technologies.
2. `<thead>`: header of the table, uses `<th>` to define cells. `<tbody>`: describes body content. Uses `<tr>` to define rows & `<td>` to define data cells. `<tfoot>`: footer of the table, typically has summaries. Used with `<th>` or `<td>` to define footer cells.

___

[Introducing Constructors](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics#introducing_constructors)

### *Questions*

1. What is a constructor and what are some advantages to using it?
2. How does the term `this` differ when used in an object literal versus when used in a constructor?

### *Answers*

1. A constructor is a standard method for the creation of an object and sets default values. It helps manage the use of an object.
2. In an O.L. it refers to the object itself that is being defined. In a constructor it refers to the object being created.

___

[Object Prototypes Using a Constructor](https://ui.dev/beginners-guide-to-javascript-prototype)

### *Questions*

1. Explain prototypes and inheritance via an analogy from your previous work experience.
    - Note: this is a very common front end developer interview question.

### *Answers*

1. As an Electronics Technician in the USCG I often installed and maintained navigation systems. Later in my CG career I was stationed at the unit and in the department that managed the support, design, and overall life cycle of the Scalable Integraded Navigation System (V2). We had one overall suite of equipment (prototype) but customized packages for each individual vessel type (object). The 25' RBS and 87' WPB and 210' WMEC have different needs, capabilities, and space available. So we maintained the overall large suite of options but derived specific setups per vessel type.

___

### *Bookmark and Review*

[HTML Table Advanced Features and Accessibility](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Advanced)
