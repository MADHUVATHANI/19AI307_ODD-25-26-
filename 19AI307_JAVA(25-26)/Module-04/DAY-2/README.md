# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:

You are developing a YouTube-like platform. Each channel can have multiple subscribers (viewers).
Whenever the channel uploads a new video, it must instantly notify all of its subscribers.
Each subscriber prints their own message like:
"[SubscriberName]: New video from [ChannelName]! Watching now..."
The channel doesn't care who the subscribers are or how many there are—it just broadcasts the update.
Student's Objective:
Implement the Observer Pattern:
Channel = Subject
Subscriber = Observer
When a video is uploaded, all subscribed users are notified.
Notifications should include channel name and video title.
## AIM:
To implement the Observer Pattern where a Channel (Subject) notifies all its Subscribers (Observers) whenever a new video is uploaded, ensuring each subscriber receives and prints a personalized notification.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number of subscribers and add each subscriber (Observer) to the channel’s subscriber list.
4.	Read the number of videos to be uploaded.
5.	For each video, call the channel’s uploadVideo() method, which prints the upload message and then triggers notifyAllSubscribers().
6.	Each subscribed Observer receives the notification and prints its personalized message, then the program stops.





## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Madhuvathani V
RegisterNumber:  212223040107
*/
```

```
import java.util.*;

interface Observer {
    void notify(String channelName, String videoTitle);
}

class Subscriber implements Observer {
    private String name;

    public Subscriber(String name) {
        this.name = name;
    }

    @Override
    public void notify(String channelName, String videoTitle) {
        System.out.println(name + ": New video from " + channelName + "! Watch now...");
    }
}

class Channel {
    private String name;
    private List<Observer> subscribers = new ArrayList<>();

    public Channel(String name) {
        this.name = name;
    }

    public void subscribe(Observer sub) {
        subscribers.add(sub);
    }

    public void uploadVideo(String title) {
        System.out.println(name + " uploaded: " + title);
        notifyAllSubscribers(title);
    }

    private void notifyAllSubscribers(String videoTitle) {
        for (Observer sub : subscribers) {
            sub.notify(name, videoTitle);
        }
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String channelName = sc.nextLine();

        Channel channel = new Channel(channelName);

        int n = sc.nextInt(); 
        sc.nextLine();
        for (int i = 0; i < n; i++) {
            String sub = sc.nextLine();
            channel.subscribe(new Subscriber(sub));
        }

        int v = sc.nextInt(); 
        sc.nextLine();
        for (int i = 0; i < v; i++) {
            String title = sc.nextLine();
            channel.uploadVideo(title);
        }
    }
}
```






## OUTPUT:

<img width="1211" height="407" alt="image" src="https://github.com/user-attachments/assets/f8337d06-e894-4127-8e95-bc314e4243f3" />


## RESULT:

Thus, the program is executed successfully.

