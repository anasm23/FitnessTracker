# FitnessTracker

## User Story
As a user, I want to be able to view create and track daily workouts. I want to be able to log multiple exercises in a workout on a given day. I should also be able to track the name, type, weight, sets, reps, and duration of exercise. If the exercise is a cardio exercise, I should be able to track my distance traveled

## Description
This application uses MongoDB, Mongoose, Express and Node to present a visualized dataset of your Workout. The user inputs their workout choosing either "Resistance" or "Cardio" and filling out the necessary details. This application uses the MVC Framework. Once the workout is created, the data is presented through both a bar and line graph over the span of 7 days.  

## Instructions
```
1. Clone repository
2. npm i 
3. npm start 
```
## Code snippets
```
const WorkoutSchema = new Schema({
  day: { type: Date, default: Date.now},
  exercises: [{
      type: {
        type: String,
        trim: true,
      },
      name: {
        type: String,
        trim: true,
      },
      duration: Number,
      weight: {
        type: Number,
        default: 0
      },
      reps: {
        type: Number,
        default: 0
      },
      sets: {
        type: Number,
        default: 0
      },
      distance: {
        type: Number,
        default: 0
      }}],
  totalDuration: {
    type: Number,
    default: 0,
  }
});
```


## Demo
<img src="assets/gif.gif"></img>

## Link to deployed site
https://sheltered-citadel-62771.herokuapp.com/exercise
