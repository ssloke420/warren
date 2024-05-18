# Warren across the lanuages

## Python
```python
import random
class Warren:
    def __init__(self, skill, age, *games):
        self.skill = skill
        self.age = age
        self.games = games
        self.events = ["got hit by a truck", "deleted his Pokemon save file", "jumped off a cliff"]

    def skilling(self):
        print("Warren performed", self.skill)
    
    def aging(self):
        age += 1
        print("Warren is now", self.age)

    def event(self):
        print("Warren", random.choice(self.events))
    def play(self):
        print("Warren played", random.choice(self.games), "for 2000000 hours")

boot = Warren("grinding", 13, ["Taming", "Pokemon", "Getting over it", "Fortnite"])
run = True
while run:
    action = input("What would you like Warren to do? ")
    if action == "quit":
        break
    elif action == "skill":
        boot.skilling()
    elif action == "age":
        boot.aging()
    elif action == "event":
        boot.event()
    elif action == "play":
        boot.play()
    else:
        print("Invalid Option")
```

## C++
warren.cpp
```c++
#include <iostream>
#include <string>
using namespace std;
class Warren {
    public: 
        int age;
        string skill;
        string game;
        Warren(int a, string s, string g){
		    age = a;
		    skill = s;
		    game = g;
        }
    void skilling() {
        cout << "This Warren performed " << skill << endl;
    }
    void aging() {
        age++;
        cout << "Warren is now " << age << endl;
    }
    void play() {
        cout << "Warren grinded " << game << endl;
    }
};  

int main() {
    Warren boot(13, "grinding", "taming");
    bool run = true;
    string action;
    while (run) {
            cout << "What would you like Warren to do? ";
            cin >> action;
            if (action == "age") {
                boot.aging();
            } else if (action == "skill") {
                boot.skilling();
            } else if (action == "quit") {
                run = false;
            } else if (action == "play"){
				boot.play();
			} else {
                cout << "Invalid option";
            }
        }
    return 0;
}
```

## Java
Warren.java
```java
import java.util.Random;
public class Warren {
	private int age;
	private String skill;
	private Games game;
	private String[] events;
	Random rand = new Random();
	public Warren(int age, String skill, Games game){
		this.age = age;
		this.skill = skill;
		this.game = game;
		this.events = new String[] { "got hit by a truck", "deleted his Pokemon save file", "Jumped off a cliff" };
	}
	public void skilling(){
		System.out.print("This Warren performed ");
		System.out.println(this.skill);
	}
	public void aging() {
		this.age += 1;
		System.out.print("Warren is now ");
		System.out.println(this.age);
	}
	public void play() {
		System.out.print("Warren grinded ");
		System.out.println(this.game);
	}
	public void event() {
		int index = rand.nextInt(2);
		String curr_event = this.events[index];
		System.out.print("Warren ");
		System.out.println(curr_event);
	}
}
```
Main.java
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        Warren boot = new Warren(13, "grinding", Games.TAMING);
        boolean run = true;
        
        while (run) {
            System.out.println("What would you like Warren to do?");
            String action = input.nextLine();
            
            if (action.equals("age")) {
                boot.aging();
            } else if (action.equals("skill")) {
                boot.skilling();
            } else if (action.equals("quit")) {
                run = false;
            } else if (action.equals("play")){
				boot.play();
			} else if (action.equals("event")){
				boot.event();
			} else {
                System.out.println("Invalid option");
            }
        }
    }
}

```
## SQL
```sql
SELECT skill, age
FROM Warren
WHERE name = 'boot'
```
Output:
|Skill|Age|
|----|----|
| Grinding| 13|
