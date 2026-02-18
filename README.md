# GDIM32 In Class Activities
## W1 In-class Activity
### Activity 1
We need to understand the playtester feedback and the error alerts, and then make the necessary code changes based on the instructions. This helps us find bugs, fix mistakes in the code, and improve the overall gameplay experience. By carefully reviewing what playtesters experienced, we can see which parts of the game are confusing or not working correctly. After making changes, we will test the game again to make sure the problems are fixed and the game feels better to play.
### Activity 2
1. x=10
2. x=2
3. The Update() method calls PrintMessage(), the PrintMessage() method outputs the text "hello world".
4. It should be replaced with MonoBehaviour.
5. The Start() method calls PrintMessage(10), passing 10 as an argument. And the PrintMessage(int x) method receives the argument x and outputs the text "x = 10".
6. Name: The highlighted line (10) is an argument. Purpose: It provides the value 10 to the PrintMessage method when PrintMessage is called in Start(), so PrintMessage uses this value as the x parameter.
7. The error is that Transform.Translate(_direction) is called on the Transform class (static context), but Translate is an instance method.
8. _playerTransform.Translate(_direction);
### Activity 3
[MG1 breakdown Google doc](https://docs.google.com/document/d/1RY8G4u76Aeqqu-rppdIJhAqMhHotRh3U2m445UlfjAs/edit?usp=sharing)


## W2 In-class Activity
### Activity 1
<img width="2360" height="1640" alt="IMG_1243" src="https://github.com/user-attachments/assets/1c4d7ca0-43a2-4344-b9ae-a946ba08bb18" />

### Activity 2

[New commit for MG2](https://github.com/UCI-GDIM32-W25/mg2-PeiyiXiong/commit/e77ea4e54d3c889397ac9ed27665bbbed9db78d7)


## W3 In-class Activity
### Activity 0-2
partner name：Yuxin Ding
### Activity 3
<img width="2360" height="1640" alt="IMG_1249" src="https://github.com/user-attachments/assets/543aaa21-81b6-4f00-908e-ead769e95851" />

## W4 In-class Activity
### Activity 0
Buddy's name： Jingyi Bi
### Activity 1
I added multiple Locators, when I ran the game and pressed the space bar, only one Locator would remain while the others would be destroyed. Because Locator class implements the Singleton design pattern.
### Activity 2
![IMG_1250](https://github.com/user-attachments/assets/079ab1ae-c209-4179-b2b3-1b638c5f352e)
### Activity 3
[New commit for MG4](https://github.com/PeiyiXiong/HW4/branches)

I successfully received hw4, then I downloaded the pictures of the birds and the pipes, and I sliced them. I changed the background size to be vertical. I created a new ground and added a component to this ground.

## W5 In-class Activity
### Activity 1
#### 1. What do you think of the design of these interfaces and abstract classes?
The design makes sense and follows the basic rules of object-oriented programming. For example, all items must follow the Use() contract that the abstract Item class has. This makes sure that they all work the same way. The IBreakable interface, on the other hand, separates the break and damage functions that not all items need. This separation makes sure that only the right items use breakable logic, and all items follow the same Use() rule. This is a clear and adaptable base for a simple item system. It doesn't add any extra ways to break items that can't break, like ElvenSword. This is in line with the principle of interface segregation.

#### 2. Would you keep it the same, or change it, if you were building a project with items like these?   
I would keep the basic structure (the abstract Item class and the IBreakable interface), but I would make small, useful changes for use in production:
- To avoid repeating code in Axe and Torch, add a BreakableItem base class that includes shared durability and state logic.
- For inventory and UI integration, give the Item class shared properties like name and ID.
- To make it work with other systems (like automatically taking broken items out of the inventory), add an OnItemBroken event to the IBreakable interface.

  
These changes fix problems with duplicate code and add useful features for real-world projects, all while keeping the best parts of the original design. You don't need to change the basic relationships between inheritance and interfaces.

### Activity 2
- Model: EnemyStats, ItemW5Demo2
- View: DialogueBubble, InventoryUI, SpriteRenderer (in PlayerW5Demo2/EnemyW5Demo2)
- Controller: PlayerW5Demo2 (movement/input logic), EnemyW5Demo2

### Activity 3
#### Scenario 1: Rhythm Game
Inheritance with Polymorphism + Basic Parent/Abstract Class/Interface + ScriptableObjects
- Create abstract `Beat` class/`IBeat` interface, define core properties: key, screen location, timing. Abstract `Spawn()/CheckHit()` methods.
- Polymorphic child classes (like `TapBeat`, `HoldBeat`, `SlideBeat`) override abstract methods for unique behavior.
- You can use ScriptableObjects to save data for each beat (timing, key, position) that can be changed in Unity without having to change any code.
  
#### Scenario 2: Team Shooter
Inheritance with Polymorphism + Basic Parent/Abstract Class/Interface + MVC with C# Events
- Base abstract `ShooterCharacter` class (inherits from MonoBehaviour; shared: health, mesh, basic movement/animation logic; abstract like `PrimaryAttack()/SecondaryAttack()/Ultimate()`).
- Polymorphic child classes (per character) override abstract attack methods for unique abilities. Implement movement modes via custom interface (like `IMovable` for sprint/air dash).
- MVC: Controller (character input/logic)-> Model (health/ability state)-> View (animations/meshes). C# events for attack/health change to trigger View/feedback.

#### Scenario 3: Farming Simulation
Inheritance with Polymorphism + Basic Parent/Abstract Class/Interface + ScriptableObjects + Finite State Machine with Enums
- Abstract `FarmObject` class/`IFarmInteractable` interface shared: position; abstract `Interact()/Grow()/Destroy()`; polymorphic children `Seed`, `GrowablePlant`, `Rock`.
- ScriptableObjects store farm object data growth time, harvest yield, interact rewards, easy editing of plant/rock properties.
- Player FSM enum: `Idle`, `Planting`, `Harvesting`, `BreakingRock` to manage state-specific animations/actions; FSM controls which interaction/animation triggers on input.

### Activity 4
Attendance: Peiyi Xiong, Jingyi Bi, Ruixuan Pan (She has asked the professor for leave and attended half of today's class.)

Proposal: [Final Project Proposal First Draft](https://docs.google.com/document/d/1xBZf-TNesHDRlNGUnQIIlStqfWb3MOsQMGyXhkQuQ5s/edit?tab=t.0#heading=h.59jtu6yosw9c)

## W6 In-class Activity
### Activity 1
- Unity Profiler: It can help me solve the problem of game lag. With Profiler, I can directly identify the cause of the lag, ensuring that the project runs smoothly. 
- Gizmos: I can use Gizmos to draw the delivery route for takeout orders. Also, with Gizmos, I can directly mark the location of the customer's home within the scene. I can also use it to draw the interaction area, such as the interaction trigger zone for the restaurant owner. Player must approach to click "I/E". By drawing a circle with Gizmos, it will be clear how close one needs to be to trigger the action.
- Breakpoints: It can help me precisely identify code errors.
- Merging: When multiple team members are changing the scene, it will help us not disrupt each other's work.

### Activity 2
Attendance: Peiyi Xiong, Jingyi Bi, Ruixuan Pan

Proposal: [Final Project Proposal Draft](https://docs.google.com/document/d/1xBZf-TNesHDRlNGUnQIIlStqfWb3MOsQMGyXhkQuQ5s/edit?tab=t.0#heading=h.59jtu6yosw9c)


## W7 In-class Activity
### Activity 1
Note: I control the chick using the WASD keys, the chick can move forward, backward, left, and right. When the chick approaches the duck, the duck will follow the chick until the chick moves away from the duck or hides behind an obstacle (when the duck cannot see the chick).
### Activity 2
Attendance: Peiyi Xiong, Ruixuan Pan

