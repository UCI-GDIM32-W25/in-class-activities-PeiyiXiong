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
I added multiple Locators, when I ran the game and pressed the space bar, only one Locator would remain while the others would be destroyed.




