# CS360-7-3-Portfolio
<!-- README.md -->

<h1>Project Three — Event & Reminder App</h1>

<h2>Briefly summarize the requirements and goals of the app you developed. What user needs was this app designed to address?</h2>
<p>
The app helps users create events, set reminders, and optionally receive SMS notifications. The main goals were to make adding and managing events fast, keep data local with SQLite for privacy, and request only the permissions truly needed. The target user need was simple daily organization without a complex learning curve.
</p>

<h2>What screens and features were necessary to support user needs and produce a user-centered UI for the app? How did your UI designs keep users in mind? Why were your designs successful?</h2>
<ul>
  <li><strong>Event List Screen</strong> shows upcoming items with clear titles, dates, and quick actions.</li>
  <li><strong>Add / Edit Event Screen</strong> captures title, date, time, and reminder options with large tap targets.</li>
  <li><strong>Reminder Settings</strong> lets users choose local notifications and optionally enable SMS.</li>
  <li><strong>Permission Rationale</strong> explains why SMS is requested only when the user turns it on.</li>
  <li><strong>Empty/Error States</strong> guide first-time users and recover gracefully from mistakes.</li>
</ul>
<p>
Design choices focused on clarity: one primary action per screen, consistent button placement, readable typography, and short labels. These decisions reduced friction, which made the UI feel simple and helped users complete tasks on the first try.
</p>

<h2>How did you approach the process of coding your app? What techniques or strategies did you use? How could those techniques or strategies be applied in the future?</h2>
<p>
I built in vertical slices, wiring each feature end-to-end before moving on. For data, I used a small repository layer over SQLite to keep UI code clean. I committed often, kept functions short, and wrote clear names for classes and methods. I also deferred dangerous permissions until they were actually needed. These strategies scale to future projects by improving readability, making bugs easier to find, and keeping feature work focused from UI to data in small increments.
</p>

<h2>How did you test to ensure your code was functional? Why is this process important, and what did it reveal?</h2>
<p>
I tested on both the Android Emulator and a real device. Device testing surfaced timing issues with notifications and the SMS permission flow that the emulator did not show. I also performed task-based checks, such as “create an event and receive a reminder,” to verify real user paths. This process was important because it caught edge cases early and improved the overall reliability of the app.
</p>

<h2>Consider the full app design and development process from initial planning to finalization. Where did you have to innovate to overcome a challenge?</h2>
<p>
I had to balance a minimal-permission approach with the SMS feature. The solution was to make SMS entirely optional, request it at the point of need, and provide a short, plain-language rationale screen. This kept the core app fully usable without SMS while still offering power users the extra option.
</p>

<h2>In what specific component of your mobile app were you particularly successful in demonstrating your knowledge, skills, and experience?</h2>
<p>
The end-to-end event flow was the strongest piece: creating an event, saving it to SQLite, scheduling a local reminder, and reflecting changes instantly in the UI. This showed solid separation of concerns, careful permission handling, and user-centered design that emphasized clarity and speed.
</p>
