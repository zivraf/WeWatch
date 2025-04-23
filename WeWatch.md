# Overview
We all like to watch TV.  
Today, we have an infinite collection of titles to pick from. However, with everything available for us to watch , it is becoming harder and harder to find what to watch.
WeWatch is a social platform (web application) helping us to select what to watch.
 
# Main scenarios:
- Users’ signUp to WeWatch given their google, or Facebook identities.
- Users pick titles they’ve watched and rate them (ranging from 1 to 5 stars). 
- Users build their social circle (identify friends) who are already signed up to the platform. 
- Given global rating, user's rating, and their social circle, WeWatch shall be able to generate recommendations to propose more titles to watch.
 

# Platform Design
A comprehensive breakdown of the system architecture and components.
## System Architecture Overview
WeWatch will be built as a web application with the following high-level components:

* Frontend: User interface for interactions
* Backend API: Core business logic implementation
* Database: User data, ratings, social connections storage
* Authentication Service: Managing user identity
* Recommendation Engine: Generating personalized recommendations

## System components
### User Management
This component handles user authentication, profile management, and account operations:

* OAuth integration with Google and Facebook for simplified signup/login
* User profile creation and management
* Account settings and preferences
* Privacy controls
* Account deletion functionality with data handling policies

### Social Network
This component manages user connections and social interactions:

* Friend discovery mechanisms according to name .
* Friend requests and connection management. A request requires approval
* Social circle visualization
* Invitation system for non-members with referral tracking
* Privacy settings for social sharing

### Title Rating System
This manages the core rating functionality:

* Title search interface connecting to both internal database and external IMDB API
* Rating mechanism (1-5 star system)
* Rating history and management
* Curated initial content (IMDB top-ranked titles)
* speed rating. Serve me with titles from IMDB (according to some filter) for me to rak.
* Personal viewing history tracking
* Personal watch list thatincludes movies the user identifies forhimself and want to remember.

### Recommendation Engine
This implements the various recommendation algorithms:

* Title Matching Algorithm: Finds similar titles based on collaborative filtering
* History-Based Profiling: Creates user profiles based on rating patterns
* Social Circle Recommendations: Surfaces titles popular among friends
* Recommendation caching and refresh mechanisms
* Feedback loop for recommendation improvement



