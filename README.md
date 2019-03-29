# DesignPatternSample

﻿http://www.dofactory.com/net/facade-design-pattern

The classes and objects participating in this pattern are:

Facade   (MortgageApplication)
	knows which subsystem classes are responsible for a request.
	delegates client requests to appropriate subsystem objects.
Subsystem classes   (Bank, Credit, Loan)
	implement subsystem functionality.
	handle work assigned by the Facade object.
	have no knowledge of the facade and keep no reference to it.


http://www.dofactory.com/net/factory-method-design-pattern

	The classes and objects participating in this pattern are:

Product  (Page)
	defines the interface of objects the factory method creates
ConcreteProduct  (SkillsPage, EducationPage, ExperiencePage)
	implements the Product interface
Creator  (Document)
	declares the factory method, which returns an object of type Product. Creator may also define a default implementation of the factory method that returns a default ConcreteProduct object.
	may call the factory method to create a Product object.
ConcreteCreator  (Report, Resume)
	overrides the factory method to return an instance of a ConcreteProduct.

http://www.dofactory.com/net/strategy-design-pattern

 The classes and objects participating in this pattern are:

Strategy  (SortStrategy)
	declares an interface common to all supported algorithms. Context uses this interface to call the algorithm defined by a ConcreteStrategy
ConcreteStrategy  (QuickSort, ShellSort, MergeSort)
	implements the algorithm using the Strategy interface
Context  (SortedList)
	is configured with a ConcreteStrategy object
	maintains a reference to a Strategy object
	may define an interface that lets Strategy access its data.

http://www.dofactory.com/net/observer-design-pattern
Subject  (Stock)
	knows its observers. Any number of Observer objects may observe a subject
	provides an interface for attaching and detaching Observer objects.
ConcreteSubject  (IBM)
	stores state of interest to ConcreteObserver
	sends a notification to its observers when its state changes
Observer  (IInvestor)
	defines an updating interface for objects that should be notified of changes in a subject.
ConcreteObserver  (Investor)
	maintains a reference to a ConcreteSubject object
	stores state that should stay consistent with the subject's
	implements the Observer updating interface to keep its state consistent with the subject's
