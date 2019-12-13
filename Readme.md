# Sample application: RavenDB, KnockoutJS, Bootstrap and more with Eugene

While learning a new technology or framework, I always like to build small but well covering Proof Of Concept application. It is even better if one can combine several new technologies into such a project. This is description of one such project. Single page web app using RavenDB, WebAPI, KnockoutJS, Bootstrap, D3JS. Available on GitHub

![alt funny jerry](https://raw.githubusercontent.com/funnyjerry/D3-University/master/screenshots/screen.png)


# The Use Case


Everyone renting an apartment or any other property knows that it might be quite difficult to track the expenses and income in order to assure himself of the rent-ability of the given property. I have created an applications which helps with just that and thanks to this applications I was able to lern the mentioned technologies. Now let’s take a look at them closer.

KnockoutJS - to glue the interaction on the client side. Knockout is one of the cool JavaScript MV(*) frameworks which provide a way to organise and facilitate the JavaScript development. Unlike other frameworks (Backbone or Ember) KnockoutJS concentrate itself only on binding of the data and actions between the GUI (HTML) and the ViewModel (JavaScript) and does not take care for other aspects (such as client side routing). The framework is very flexible and allows you to bind almost anything to any DOM’s elenent value or style.
RavenDB - to stored the data. RavenDB is a document database, which seamlessly integrates into any C# project.
WebAPI - to serve the data through REST services. WebAPI is a quite new technology from MS which is meant to provide better support for building REST services. Of course we have built REST services with WCF before, so the questions is why should we change to WebAPI? WCF was created in the age of WSDL. It was adapted later to generate JSON, however inside it still uses XML as data transformation format. WebAPI is complete rewrite which also provides other interesting features.
Bootstrap - to give it a decent GUI. As its name says, bootstrap enables a quick development of a web application’s GUI. It is a great tool to all of us who just want to get the project out and we still need a decent user interface.
D3.js - to visualize data using charts. D3JS is a JavaScript library enabling the user to manipulate the DOM and SVG elements.
KoExtensions - very small set of tools which I have created, allowing easy creation of pie charts or binding to google maps while using KnockoutJS.


# The architecture of the application

The architecture is visualized in the following diagram. The backend is composed of MVC application, which exposes several API controllers. These controllers talk directly to the database through RavenDB IDocumentSession interface. The REST services are invoked by ViewModel code written in JavaScript. The content of the ViewModels is bound the view using Knockout. 


![alt funny jerry](https://raw.githubusercontent.com/funnyjerry/D3-University/master/screenshots/architecture.png)
