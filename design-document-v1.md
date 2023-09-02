# "Beacon" App

*Software Design Document*

---

## Contents

- Purpose
- Concept
- Features (PoC)
- Technology

## Purpose

This project is a response to the tedious process of searching for and scheduling of common activities via standard modes of communication (text/call). The aim is to make the process of searching, creating, and/or subscribing to an activity intuitive and less reliant on inefficient modes of scheduling.

## Concept

Within a rotating window throughout the week, a user is able establish some kind of communication with what we'll call a 'beacon' representing some kind of activity at some location. A user can passively observe the state of an existing beacon, subscribe to it, or create one of their own. Information can be observed about the activity like:

- Participants
  - how many
  - names
  - availability
- Activity
  - type
  - location

The idea is best expressed as a literal beacon -- if the beacon is off, no one is around/interested. If the beacon is on, someone is around/interested. From there the user can act on this information in a few simple ways. The timeframe is intended to be short (1-12 hours depending on the activity) to ensure high levels of commitment, remain intuitive, and avoid scheduling fatigue.

## Features (PoC)

### Account

Accounts should be *bare bones*.

- Email
- Password
- Name

### List/Map

- List of beacons with relevant info
- Map with interactive location pins (beacons)

### Friends List

Users will have the ability to connect with each other to respond to private beacons.

### Beacon Interaction

#### RSVP

The most common form of interaction will likely be responding to existing beacons. This will be done by merely indicating your attendance by pushing a toggle button (going/not going).

#### Subscription

The second most common form of interaction will likely be subscribing. This can occur in 3 ways:

- Subscribing to a particular beacon (perhaps this is a beacon that has a fixed location, i.e. a park)
- Subscribing to a particular activity
- Automatic subscription through RSVP

#### Creation

Finally, a user can create a beacon. This will require the creator to move through a simple flow to choose the activity and preferred time. Beacon creation is limited in 2 ways:

- Specific location -- can only share privately between friends
- Select public locations (i.e. a basketball court)

### Timeframes & Lifespan

As stated before, the intention is to avoid definitive times and scheduling and to work within relative, short timeframes.

##### Timeframe Rules

- No specific times can be selected (e.g. starts @ 5PM)
- Timeframes will be between 10-120 minutes (subject to change)

##### Lifespan Rules

- A beacon cannot represent an activity any earlier than 1 hour (subject to change) before the defined timeframe. This is to give a reasonable amount of time for people to respond
- A beacon will expire after the upper limit of the timeframe is reached

### Prospective Activities

- basketball
- lunch
- gym

## Technology

The first iteration of this will purely be front end based with mock data used for dummy endpoints. This is to focus more on establishing a PoC, getting user feedback, and iterating the UI/UX. Backend work will come if and when the PoC proves the app is feasible.

### Stack  (not final)

- React
  - Jest
  - RTL
- Typescript
- Webpack