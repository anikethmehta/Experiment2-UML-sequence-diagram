### ***Date*** : 6 August 2023
### ***Title*** : LAB 4 UML-sequence-diagram

### ***Aim*** : To design UML sequence diagram

### ***Theory*** : What is a Sequence Diagram in UML?
UML Sequence diagrams are interaction diagrams that detail how operations are carried out. As sequence diagrams can be used to capture the interaction between objects in the context of a collaboration, one of the primary uses of sequence diagrams is in the transition from requirements expressed as use cases to the next and more formal level of refinement. Use cases are often refined into one or more sequence diagrams.Sequence diagrams are time focus and they show the order of the interaction visually by using the vertical axis of the diagram to represent time what messages are sent and when.

### Sequence Diagrams captures interaction in different level of granularity:

1. high-level interactions between user of the system and the system, between the system and other systems, or between subsystems (sometimes known as system sequence diagrams)
2. the interaction that takes place in a collaboration that either realizes a use case or an operation (instance diagrams or generic diagrams)
3. Represent objects interact in (Model, View / Controller) MVC pattern of software framework


### ***Explanation*** : When to Draw Sequence Diagram?
1. Model high-level interaction between active objects in a system
2. Model the interaction between object instances within a collaboration that realizes a use case
3. Model the interaction between objects within a collaboration that realizes an operation
4. Either model generic interactions (showing all possible paths through the interaction) or specific instances of a interaction (showing just one path through the interaction)

### How to Draw a Sequence Diagram?
1. Identify a set of objects that will participate in the general collaboration (or use case scenario)
   
   1. If you derive the sequence diagram based on a scenario of a use case, select the normal scenarios first
      
   2. You should know the primary actor(s) who activates the use case
   
2. Consider the first point of the scenario (or if you get it from the first point of the flow of event of a use case)
   
3.  Consider what the system need to be done in order to response to the actor, when the actor send the message to the system
   
    1. What the system need to be handled before the return message response back from the system?
      
    2. E.g. A customer inserted an ATM card to the machine, the system will display "input pin number" in the normal scenario, right?
      
    3. Guess, what will to be handled inside the ADM by a set of objects at the "back" of the system? Something like, read and verify the ATM card (card reader), read the 
      card information of the card holder (by the bank) and ask for the pin, or, return "invalid card type, insert another card", and etc.
    
    4. By this way, you will identify the candidate objects and operations of the target application for that particular scenario and you can also use these information as 
      a basis to derive the class diagram incrementally.
      
    Repeat each of the point of the scenario (or flow of event) and until you complete all the points in the scenario.

### Components of Sequence diagram: 
1.***Lifeline***

A lifeline represents an individual participant in the Interaction.

2.***Actor***

An Actor a type of role played by an entity that interacts with the subject (e.g., by exchanging signals and data). An actor can also be an external to the subject (i.e., in the sense that an instance of an actor is not a part of the instance of its corresponding subject). They typically represent roles played by human users, external hardware, or other subjects.

3.***Activation***

An activation is represented by a thin rectangle on a lifeline) represents the period during which an element is performing an operation. The top and the bottom of the of the rectangle are aligned with the initiation and the completion time respectively

4.***Call Message***

A call message defines a particular communication between lifelines of an interaction, which represents an invocation of operation of target lifeline.

5.***Return Message***

A return message defines a particular communication between lifelines of an interaction, which represents the pass of information back to the caller of a corresponded former message.

6.***Self Message***

A self message defines a particular communication between lifelines of an interaction, which represents the invocation of message of the same lifeline.

7.***Recursive Message***

A recursive message defines a particular communication between lifelines of an interaction, which represents the invocation of message of the same lifeline. It's target points to an activation on top of the activation where the message was invoked from.

8.***Create Message***

A create message defines a particular communication between lifelines of an interaction, which represents the instantiation of (target) lifeline.

9.***Destroy Message***

A destroy message defines a particular communication between lifelines of an interaction, which represents the request of destroying the lifecycle of target lifeline.

10.***Duration Message***

A duration message defines a particular communication between lifelines of an interaction, which shows the distance between two time instants for a message invocation.

11.***Note***

A note (comment) gives the ability to attach various remarks to elements. A comment carries no semantic force, but may contain information that is useful to a modeler.


 ### ***Output Screenshot*** :
 https://github.com/anikethmehta/Experiment2-UML-sequence-diagram/blob/main/Sequence_diagram.png
 
  
