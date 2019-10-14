# BBC News and Weather Apps (Android) Coding Challenge

## Introduction
You have been asked to kick off a new native Android news app, initially consisting of two screens
- The first screen will simply display a list of the headlines (fetched from a server - see below) and the last updated date
- When the user taps on a headline, the application then shows a second screen containing the headline and the last updated date again, as well as the introductory paragraph

The designer has asked that the typography be as follows:

Components | Color | Font
-----------| ------|------
headline | #000000 | bold, 20sp, system font (roboto)
last updated | #3d3d3d | normal,  12sp, system font (roboto) 
introductory | #000000 | normal, 14sp, system font (roboto)

The returned timestamp is in epoch time but the design calls for this to be a human readable day, month and year. So, for example, it should show as "1 January 1970" for an epoch timestamp of 0.

The user should also be able to trigger a reload of the data from the server.

### API
The list of headlines is available at
https://github.com/bbc/news-and-weather-apps-coding-challenge-android/blob/master/headlines.json

```bash
curl -G https://raw.githubusercontent.com/bbc/news-and-weather-apps-coding-challenge-android/master/headlines.json
```

### Analytics
The product manager needs you to record interaction and network events as people use the app. This can be done by issuing “fire and forget” GET requests to
https://github.com/bbc/news-and-weather-apps-coding-challenge-android/blob/master/analytics

Event specific query parameters should be appended to the URL as follows:

* `event=load` – any network request
* `time=xxx` - the time (in ms) for the network request to complete
* `event=display` – whenever a screen is shown (the headline or the article)
* `screen=XXX` - an identifier for the screen that was shown

```bash
curl -G https://raw.githubusercontent.com/bbc/news-and-weather-apps-coding-challenge-android/master/analytics?event=load&time=100
```

```bash
curl -G https://raw.githubusercontent.com/bbc/news-and-weather-apps-coding-challenge-android/master/analytics?event=display&screen=XXX
```

### Considerations
This is an opportunity to demonstrate your understanding of what modern Android app development looks like. We believe that good contributors to achieving this are typically code readability, unit testing, separation of concerns, the open/closed principle, error handling, and an intuitive, responsive, user interface.

Please write the app in Kotlin.

Remember we are looking for a demonstration of your skills - not perfection. A comment about what you would do next might be better than squeezing in everything, but not doing anything to your usual standard. We would typically expect this to take you  between 2-3 evenings at most.

### Submissions
To submit your code, please create a private GitHub repo (it’s free) and share your code repo with our GitHub user, [bbcnewsapps](https://github.com/bbcnewsapps). Please note that we will be considering your git commit history during our evaluation.

_Under no circumstances make the repository public._
_Please email your BBC Careers contact separately as well to confirm your submission._

