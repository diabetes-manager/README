# Proposal For Databetes

---

### What problem does your app solve?

Help diabetics better manage their glucose levels with continuous glucose
monitoring

### Be as specific as possible; how does your app solve the problem?

By creating an app that is easy for a user to engage with and actively manage
their disease by helping them keep track of their personalized historical
glucose readings along with other user input data in order to make near-term
predictions of glucose levels based on machine learning algorithms.

### What is the mission statement?

Improve diabetes disease management by helping users store and integrate glucose
readings and lifestyle data to help better project near-term sugar levels

---

## Features

-   What features are required for your minimum viable product?

1. Mobile friendly dashboard showing blood sugar levels
2. Model predicting blood sugar levels over the next 30 minutes to 2 hours

-   What features may you wish to put in a future release?

Add offline model predictions by using machine learning chip in phones Provide
useful feedback and insights based on the data collected and our model E.g.
“You’re blood sugar is consistently low in the morning, ask a medical
professional about adjusting your overnight basal rates.”

-   What do the top 3 similar apps do for their users?

LoopKit Guardian Connect Glooko Frameworks - Libraries

-   What 3rd party frameworks/libraries are you considering using? Greensock
    Amplify AWS React Postgres Node Express

*   Do APIs require you to contact its maintainer to gain access? Some of the
    APIs for getting the large data may need additional support

*   Are you required to pay to use the API? No, and if we run into this, we will
    drop that API for the scope of this project.

*   Have you considered using Apple Frameworks? (MapKit, Healthkit, ARKit?) Yes.
    For Data Scientists

-   Describe the Established data source with at least rough data able to be
    provided on day 1.
-   You can gather information about the data set you’ll be working with from
    the project description. Be sure to collaborate with your PM, and your
    Backend Architect to chat about the resources you have.
-   Write a description for what the DS problem is (what uncertainty/prediction
    are we trying to do here? Sentiment analysis? Why is this a useful solution
    to a problem?)
-   A target (e.g. JSON format or such) for output that DS students can deliver
    to web/other students for them to ingest and use in the app

[ The data science problem is predicting a continuous glucose level at a future
time (within two hours). The major features are the historical glucose readings
and other lifestyle and physiological factors such as dietary details, exercise,
amount of sleep, and heart rate. This is a time series sequence problem. Glucose
levels can be highly variable depending on current levels and the type of food
intake. The initial training data will be customized to one or two individuals
due to difficulty of data access and the value of customized personal
healthcare. Going forward the model accuracy potentially could improve by
factoring some weight in a larger number of individuals but the likely important
features will still be the user’s personalized historical readings and detailed
food intake data.Our initial idea is to try baseline time series methods,
gradient boosted trees, and a recurrent neural network (long short-term memory).
The current problem has two main issues that data science and this proposed app
could help solve. First, data is not well integrated and secondly the data is
not used for prediction but instead requires diabetics to make rough judgments
based on experience and high level physician recommendations. The app can
potentially help diabetics become better aware of the impact of food and other
lifestyle factors have on their near term glucose levels and improve their
disease management. One difficulty with data management is that we ideally want
to train data online as the user inputs new data several times a day and it
needs to feed into the model to update the predictions for the next targeted
time frame. If the app is integrated with the other wearable devices, the
continuous glucose readings and heart rate data should feed directly into a
database. Once the user inputs other necessary data and clicks on prediction,
the model should factor in the historical stored data plus other input data and
return back to the app the projected readings. Down the line other features
could be push notifications for other projections that require continuous data
flow and modeling. For example once a high reading occurs, a simulated
projection of how much time it will take until glucose decreases back to a
normal range, a projected time frame for next meal to avoid sugar levels
dropping significantly, alerts for reading errors in connected devices, a day
planner simulation (input ahead of time what an outlier day could be like that
restricts or impacts eating times like due to travel etc. and simulate what the
levels could be to help user safely plan ahead of time) and exportable data for
user to share with doctor if desired. The current thought on data format is to
convert the data results into JSON and sent to the backend system.]

Target Audience

Who is your target audience? Be specific. Type one diabetics that use an insulin
pump and a continuous glucose monitor. In our initial launch phase they will
need a web client or an android device

What feedback have you gotten from potential users? “Everything should sync
automatically, so I don’t have to manually look in multiple places for my CGM
data vs my pump data, etc” “It would be very helpful if it had push
notifications that informed me that I need to eat within the next hour and a
half to two hours” “If I test and my blood glucose is high, it should be able to
set a timer to notify me to check my glucose progress in X time. Additionally it
should be able to let me know a timeframe that my glucose should be back in a
normal range.

Have you validated the problem and your solution with your target audience? How?
[ Team members has validated this problem and potential solution with at least
one diabetic who has been willing to share personalized data for this app. There
is also secondary research that has indicated the health issues of glucose level
fluctuations and the limited user friendly options available to both integrate
different data and provide helpful near-term predictions. ]

Research

-   Research thoroughly before writing a single line of code. Solidify the
    features of your app conceptually before implementation. Spend the weekend
    researching so you can hit the ground running on Monday. Prototype Key
    Feature(s)

-   This is the “bread and butter” of the app, this is what makes your app
    yours. Calculate how long it takes to implement these features and triple
    the time estimated. That way you’ll have plenty of time to finish. It is
    preferred to drop features and spend more time working on your MVP features
    if needed.

Considerations

Users can set different bolus injection periods Normal Bolus: Injects insulin
all at once (1-2 minutes) Square Wave Bolus: Event injection distribution over
set time (30 minutes - 8 hours) Dual Wave Bolus: Combination of Normal and
Square Wave Bolus Users carb to insulin ratio differs There is a medically
accepted standard that can be used as a jump off point Ideally the prediction
model will take the standard and modify the ratio based on the users pump
setting, or observed input data (being carbs consumed and insulin given in both
basal and bolus Basal rates will differ by user and also need to be calculated,
these are usually a constant variable per user--or at least change very
infrequently Data on screenshots for marketing pages should be accurate E.g. if
the app is showing a blood glucose of 246 mg/dL it shouldn’t then suggest a 15
unit bolus as that would put them at a negative blood glucose level
