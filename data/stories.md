## happy path
* greet
  - utter_greet
* mood_great
  - utter_happy

## sad path 1
* greet
  - utter_greet
* mood_unhappy
  - utter_cheer_up
  - utter_did_that_help
* affirm
  - utter_happy

## sad path 2
* greet
  - utter_greet
* mood_unhappy
  - utter_cheer_up
  - utter_did_that_help
* deny
  - utter_goodbye

## say goodbye
* goodbye
  - utter_goodbye

## bot challenge
* bot_challenge
  - utter_iamabot

## check weather path
* greet
  - utter_greet
* query_current_weather
  - action_current_weather
* query_current_weather
  - action_current_weather
* goodbye
  - utter_goodbye

## current weather path
* query_current_weather{"GPE":"london"}
  - action_current_weather

## New Story
* greet
    - utter_greet
* query_current_weather{"GPE":"london"}
    - slot{"GPE":"london"}
    - action_current_weather
    - utter_goodbye
