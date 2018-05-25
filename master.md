# Apps Script API

A master doc (of sorts) for the Google API ecosystem. 

## What is Apps Script? 

Google Apps Script is a javaScript based scripting language that provides persons with greater control and capabilities when using G Suite products. These services provide robust and highly beneficial functionality without the need to install any new hardware. The scripts run provide for rapid deployment as they run on Google's servers, which drastically reduces necessary development time.

The Apps Script services can be categorised into three main categories;-

1. G Suite services
    1b. provides access to the G Suite grouo of apps/services, like Drive, Sheets or Docs. 
1. Advanced Google services
    1b. facilittates access to Google APIs, which includes the G Suite product APIs. These services must be enabled before use
1. Script services
    1b. connects to utitlity services which are not directly part of a G Suite product. 

As always, Google's official documentation remains the most comprehensive source for information on Apps Script. However, several independent sites like this exist that provide tutorials, guides or snippets. Additionally, Google Developers Lab maintains a Youtube channel, dedicated blog, codelabs and other forms of disseminating information to interested parties. Books can be obtained as well from sites like Amazon or O'reilly. Developers or freelancers can be contracted for specific or complicated applications. Important to note is that there are many sources of useful information available; whether at a cost or for free. 

*** don't call is GAS***

Breakdown
1. G Suite Service (ie top level object)


1. Objects (top-level / parent)
    1.1. Classes  (child)
        1.1.1 Properties
        1.1.2. Methods
    1.2. Methods
    1.3. Interfaces
    1.4. Methods
?? where do enums fit...enums are properties of the top level?



Each service contains at least one global, top-level, object that serves as the entry point. These global objects have methods that when invoked return either data or a class. If the methid returns anothe Apps Script class, additional methods can be chained on the same line. 

Some services have more classes with corresponding properties and methods than others. Generally speaking, the tasks to be executed by that service dictates the number of classes, properties and methods. For example, the SpreadSheetApp, which is the entry pioint for tasks specific to a Google Sheet has approximately 35 classes. Each of which has its own set of properties and methods. Not to mention that Google is continuosuly releasing new functionality. At the time of the writing, the most recent release dated April 23, 2018 contained close to 20 new SpreadsheetApp methods supporting connectivity with Groups.

Child classes are not always accessed using the method of a global object.  As a matter of fact, each service contains these child classes that can only be accessed by calling a method that returns it. 

A portion of services also include special classes that are labelled as interfaces. These are generic classes that return items which may not be defined in advance. For example, the Document service method Body.getChild(childIndex) returns a generic element that could be a Paragraph, Table, List Item etc. 

Enumerated Types are key-value pairs used to define settings. In almost all cases, the enums are accessed from the global object

## How useful is it.....really?

Very useful. It's openness is one of its key advantages. The options are virtually limitless and can be tailored to almost any specfic need. Furthermore, existing processes can be tweaked to allow G Suite products to do more of the 'heavy-lifting' we are used to. If it can be calculated, Apps Script can do it in the background. If it can be written, Apps Script can automate its creation. If it can be emailed, Apps Script just needs the who, where, when and what. 

Among some common tasks are;
* create custom Google Sheets functions
* create custom menus, dialogs and sidebars for Docs, Sheets and Forms
* design add-ons to enhance functionality of G Suite products
* automate generation & submission of reports
* execute repetitve administrative tasks
* dynamically create presentations and documents
* communicate with external APIs
* and many, many more

The learning curve for becoming proficient in Apps Script is not considerably steep. Obviously, the aptitude of the individual coupled with their level of familiraity with programming techniques. Having been designed from JavaScript, persons knowledgable of that language may find the learnign process to be fairly easy. Nonetheless, all services maintain enough uniformity that its gets understanding becomes progressibvley easier as more services are explored. Important to note that most fetaures since JavaScript 1.6 are avialable (with some from 1.7 & 1.8). However because the scripts are run server-side, browser-based features such as the DOM or Window objects are not available. 

## Service Glossary

| Service | Description |
|---|---|
| Cache Service | scripts can be used to temporarily results that take time to fetch/compute |
| CalendarApp | allows for scripts to access and/or modify the user's Google Calendar or other subscribed calendars |
| Card Service | configure and build card & widget components for a UI |
| Charts Service | used to create charts for ***server-side*** rendering.  |
| ContactsApp | provides the ability to access and/or modify Google Contacts |
| Content Service | this feature allows scripts to serve text in forms such as XML or JSON |
| DocumentApp | scripts can be used to create, access or modity Google Docs files |
| DriveApp | gives the ability to create, access and modify the files and folders within Google Drive |
| FormApp | used to create, access and modify Google Forms |
| GmailApp | allows scripts that can send email, compose drafts, manage lables among many other account management tasks. Similar to MailApp but provides more customizations |
| GroupsApp | used to access Google Groups information such as querying member details |
| HTML Service | allows scripts to return HTML, generally as a UI |
| JDBC Service | used to connect scripts to JDBC compliant databases, including Google Cloud SQL, MySQL, Oracle or MS SQL server |
| LanguageApp | automatically translate text using this service |
| Optimization Service | used to model and solve linear & mixed-integer linear programs |
| Lock Service | used to prevent concurrent access to section of code which cn be useful to prevent collisions where shared resources have multiple access points |
| MailApp |solely for the sending of emails |
| Maps ??| use script to conduct Maps tasks such as generate static maps, obtain directions, convert addresses into geocode coordinates |
| Properties Service | alloows scripts to store strings as key-value pairs scoped to a specific script, user or document |
| ScriptApp | facilititates access to script triggers and publishing |
| SitesApp | used to conduct functionality to *classis* Google sites |
| SlidesApp | allows scripts to create, access and modify Google Slides flies |
| SpreadsheetApp | create, access and modify Google Sheets flies |
| UrlFetchApp | provides the ability for scripts to access other resources on the web, such as handling HTTP / HTTPS requests and responses |
| Utilities Service | provides utilities for string encoding & decoding, date formatting, JSON manpulation and other maintenance tasks |
| XML Service | allows scripts to parse, navigate and programmatically create XML documents |
