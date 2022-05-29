# Vibebox - Movie Recommendation System

## Submission for Microsoft Intern Engage 2022 

![Recommendation](https://img.shields.io/badge/Recommendation-python-blue)
![Framework](https://img.shields.io/badge/Framework-Flask-red)
![Frontend](https://img.shields.io/badge/Frontend-HTML/CSS/JS-green)
![API](https://img.shields.io/badge/API-TMDB-fcba03)
![Backend](https://img.shields.io/badge/backend-firebase-blueviolet)

Vibebox is a web application developed for Microsoft Engage 2022. As a part of this program, the mentees were provided with three tracks to choose from: Face Recognition, Data Analysis and Algorithms. I chose the algorithms track and developed a movie recommendation system, Vibebox which uses content based filtering algorithm.

<img src="static\vibe.jpg" alt="Banner" height='340' width='1000'/>
<hr>

## Table of contents
- [Technology Stack](#technology-stack)
- [Incorporating Agile Methodology](#incorporating-agile-methodology)
- [What, How of Recommendation System](#what-how-of-recommendatinone-engine)
- [Prerequisites](#prerequisites)
- [Getting started - Installation](#getting-started---installation)
- [Navigating through App](#navigating-through-app) 
- [Useful links](#useful-links)
- [Resources used](#resources-used)
- [Sources of Datasets](#sources-of-datasets)
- [Need help?](#need-help)
<hr>

## Technology Stack
<div>
      <p align="center">
        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40"/>
        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/>
        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/>
        <img src="https://github.com/devicons/devicon/blob/master/icons/python/python-original.svg" alt="python" width="40" height="40"/>
        <img src="https://github.com/devicons/devicon/blob/master/icons/flask/flask-original-wordmark.svg" alt="flask" width="40" height="40"/>
        <img src="https://www.vectorlogo.zone/logos/firebase/firebase-icon.svg" alt="firebase" width="40" height="40"/>
      </p>
</div>

- HTML, CSS and JavaScript were used for designing the frontend of the application.
- Python was used to perform data processing and develop the machine learning model.
- Firebase was used for the database and authentication feature.
- Flask was used for integrating the frontend and ML model, serving as backend.
<br/>[(Back to top)](#table-of-contents)
<hr>

## Incorporating Agile Methodology 
Agile methodology is a development strategy being adopted in the software industry. It promotes flexibility and teamwork.

SCRUM is a subset of Agile, a framework for developing software. SCRUM takes advantage of different techniques to achieve goals in Agile. SCRUM promotes an iterative model where the planning is performed on a very short term. The basic time working unit is the sprint. SCRUM teams always reason in sprints and their planning is limited to sprints.

* Sprint 1 (May 04 - May 08): **Sprint Planning and Research** - Started researching about what exactly the recommendation system is, how does it work and what are the different types of recommendation engines. Also, checked which recommendation engine is suitable for suggesting movies.0

* Sprint 2 (May 08 - May 12): **Design phase** - Started with building a basic prototype which was a simple machine learning recommendation system. Planned the UI of the website, tech stack for the project and tried incorporating the tips given by mentor.

* Sprint 3 (May 12 - May 25): **Build phase** - Developed the final web application, Vibebox which also had some extra features apart from recommending movies mentioned in [Navigating through App](#navigating-through-app).

* Sprint 4 (May 25 - May 28): **Testing phase** - Started with doing the UI fixes, did some manual testing and also uploaded the project on Github in this phase.
<hr>

## What, How of recommendation engine
### Content Based Filtering
The idea behind Content-based recommendation system is to recommend an item based on a comparison between the content of the items and a user profile. In simple words,one may get recommendation for a movie based on the description of other movies.

### Similarity Score
Similarity scoring is equivalent to seeking out points in the multidimensional space that are near enough to each other to potentially represent the same true location. It is a numerical value ranges between zero to one which helps to determine how much two items are similar to each other on a scale of zero to one.

### Cosine Similarity 
Cosine Similarity is a measurement that quantifies the similarity between two or more vectors. The cosine similarity is the cosine of the angle between vectors. The vectors are typically non-zero and are within an inner product space. Smaller angle indicates higher cosine similarity.
<hr>

## Prerequisites 
Install python from your system if not already installed from https://www.python.org/downloads/ and select it according to your system specifications.
<hr>

## Getting Started - Installation
- Clone or download this repository to your local machine.

```bash
git clone https://github.com/TechGeek3/Vibebox.git
```

- Install all the libraries mentioned in the [requirements.txt]() file with the command `pip install -r requirements.txt`
- Get your API key from https://www.themoviedb.org/ by:
    1. Create an account
    2. Click on API from left sidebar
    3. Fill the required details to apply for API Key
    4. In website URL write "NA"
    5. You'll see the API Key once approved

- Replace YOUR_API_KEY in **both** the places (line no. 16 and 32) of `static/recommend.js` file, in line no.8 of `api.js` and hit save.
- In order to run the preprocessing files download `movies_metadata.csv` and `credits.csv` from [Kaggle](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset).
- Open your terminal/command prompt from your project directory and run the file `main.py` by executing the command `python main.py`.
- Go to your browser and type `http://127.0.0.1:5000/` in the address bar.
- Finally, it's done! Enjoy the website.
<br/>[(Back to top)](#table-of-contents)
<hr>

## Navigating through App
### Sign Up & Login
<hr>
User should first register by providing the required credentials and then after successful registration, he/she can login with the previously entered details.

<p>
<img src="ReadMe\SignUp.jpg" alt="Sign Up" width="400"/>
<img src="ReadMe\LogIn.jpg" alt="Log In" width="400"/>
</p>

### Home Page
<hr>
After logging in, user will be redirected to the home page of the application where they can explore the movie banners and watch their trailer.

<img src="ReadMe\Home.jpg" alt="Home Page" width="700"/>

### Search Movies
<hr>
User can search movie details by entering the movie name which also has an **autocomplete functionality** and the respective movie poster along with overview, genres and other information will be displayed.

<img src="ReadMe\Search.jpg" alt="Search Movie" width="700"/>

### Cast Information
<hr>
One can also see the cast of the movie searched and it can be expanded to get detailed information by clicking on Know More button.

<img src="ReadMe\CastInfo.jpg" alt="Cast Information" width="700"/>

### Recommended Movies
<hr>
After scrolling the person will see the recommended movies based on the entered movie which is done with the help of ML model.

<img src="ReadMe\RecommendedMovies.jpg" alt="Recommended Movies" width="700"/>

### Sentiment Analysis
<hr>
Reviews of different users can also be found for the given movie.

<img src="ReadMe\SentimentAnalysis.jpg" alt="Sentiment Analysis" width="700"/>

### Genres Based Filtering
<hr>
In the home page, there are various categories based on genres of the movie.

<img src="ReadMe\GenreBased.jpg" alt="Genre Based Filtering" width="700"/>

### Trending Movies
<hr>
Trending movies are also updated in the home page by using TMDB API.

<img src="ReadMe\Trending.jpg" alt="Trending Movies" width="700"/>

### Logout
<hr>
Finally the user can logout with the option given in the navbar after exploring the website.

<img src="ReadMe\LogOut.jpg" alt="Logout" width="700"/>

<br/>[(Back to top)](#table-of-contents)
<hr>

## Useful Links
- [Demo Video]()
- [Sprint Document](https://www.canva.com/design/DAFB-AJnMBQ/uL28KO6ei2TdPPuK2H_XFA/view?utm_content=DAFB-AJnMBQ&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)
- [Design Document]()
<br/>[(Back to top)](#table-of-contents)
<hr>

## Resources Used
- [Recommendation System](https://www.youtube.com/watch?v=1xtrIEwY_zY)
- [TMDB API](https://www.themoviedb.org/documentation/api)
- [Getting started with Firebase Authentication](https://firebase.google.com/docs/auth/web/start)
- [Web Development using Flask](https://www.geeksforgeeks.org/python-introduction-to-web-development-using-flask/)
<br/>[(Back to top)](#table-of-contents)
<hr>

## Sources of datasets
- [The Movies Dataset](https://www.kaggle.com/rounakbanik/the-movies-dataset)
- [IMDB 5000 Movie Dataset](https://www.kaggle.com/carolzhangdc/imdb-5000-movie-dataset)
- [Movies in 2018](https://en.wikipedia.org/wiki/List_of_American_films_of_2018)
- [Movies in 2019](https://en.wikipedia.org/wiki/List_of_American_films_of_2019)
- [Movies in 2020](https://en.wikipedia.org/wiki/List_of_American_films_of_2020)
<br/>[(Back to top)](#table-of-contents)
<hr>

## Need Help?
Feel free to drop a mail on palaknj32@gmail.com
<br/>
[![Linkedin](https://img.shields.io/badge/Linkedin-Connect-blue)](https://www.linkedin.com/in/palak-jain-234384212/)
[![Twitter](https://img.shields.io/badge/Twitter-Follow-brightgreen)](https://twitter.com/palakj_03)
<br/>[(Back to top)](#table-of-contents)
<hr>
