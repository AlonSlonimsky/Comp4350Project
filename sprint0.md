## Product Vision

***BisonRides*** is a ridesharing application designed to help university 
students get to campus efficiently and reliably. Drivers can post the 
routes they regularly take to campus, along with an initial price they 
consider reasonable for providing a ride. Riders can browse available 
routes and request to join a driver’s trip, while the built-in price 
negotiation system allows both parties to settle on a mutually acceptable 
fare. If none of the available routes meet a rider’s needs, they can 
create a custom ride request that is visible to drivers, who can choose 
to accept it. The application also allows riders and drivers to 
communicate directly when arranging rides or discussing specific 
accommodations, ensuring both parties can clearly communicate their 
needs before the trip. 

The primary target audience for ***BisonRides*** is university students, 
specifically those who do not have reliable access to a personal 
vehicle, a driver’s license, or a convenient public transportation 
option. ***BisonRides*** is particularly useful for students who live in areas 
without access to public transportation or who, for personal reasons, do 
not feel comfortable using public transit. By connecting these students 
with other university students who are already travelling to campus, 
***BisonRides*** provides an additional transportation option that can better 
accommodate individual schedules and circumstances.

***BisonRides*** provides students with a flexible and reliable alternative 
to public transit, which can be especially valuable during winter months 
or for students who need to arrive on campus early in the morning for 
classes or exams. Compared with public transit, car rides can provide a 
faster and more direct means of transportation, helping students arrive 
on campus more efficiently and reliably. The application also provides 
an opportunity for students with vehicles to earn additional income by 
offering rides while encouraging carpooling among students. By increasing 
the number of students sharing rides, ***BisonRides*** can help reduce the 
number of individual vehicles travelling to campus, potentially 
decreasing traffic congestion and transportation-related carbon 
emissions. This can contribute to cleaner air and more sustainable 
transportation while providing students with a convenient way to travel. 

The success of ***BisonRides*** will be measured using several indicators of 
user satisfaction and adoption. The project will be considered successful 
if it achieves the following goals: it maintains an average user 
rating of at least 4 out of 5 stars, and a user study indicates that 
***BisonRides*** is the preferred ridesharing application among participating 
University of Manitoba students.

## Initial non-functional expectations

- **Performance**: Usable speeds. Embedded map and algorithms should not be noticable bottlenecks in frontend and backend performance respectively.

- **Reliability**: Should work reliably without crashing.

- **Security**: Safe storage of credentials/secrets. Especially payment information and user email lists.

- **Accessibility**: Follow best practices i.e. alt text on any image.

- **Availability**: Render loads in 1 minute. Should be usable from both mobile and desktop devices.

## Initial technology and platform decisions

- Deploy backend onto **Render** 

- Use **Supabase** for the DB 

- Deploy frontend website onto **Vercel** 

- **Vite**, **TS** to build frontend 

- **Resend** for sending emails or **Twilio** for sending SMSs 

- **GitHub Actions** for CI/CD pipelines, 

- **Sonar Cloud** on PR, Push 

- **Trivy** maybe on PR, Push 

- CD with **Docker** (render deploys image) 

- **Leaflet** to visualize the map on the frontend 

- **Openrouteservice** API for map calls 

- **Python**, (**Flask** or **FastAPI**) with **SQLAlchemy** 

- **Stripe** for payments 

- Caching (**Redis**) 

- **JWT** for authenticating in the frontend 

## Lightweight Architecture Sketch

![Architecture sketch](documents/ArchitectureDiagram.png)

## Additional process or protocol documentation

- 2 people review any PR before merge 

- Issues are dev tasks

- Branches resolve designated issues 

- `main` branch, `dev` branch, issue branches split from `dev` branch, infrequently carefully merge `dev` into `main` 

- `main` should always be a stable product

- Assign self to user stories with deadlines 

- Discussing tasks that need to get done on *Discord*, once decided self-assign those tasks on github 

- Create new issues as needed and assign to whoever makes sense and is available 

- Bigger issues can be discussed on *Discord* 