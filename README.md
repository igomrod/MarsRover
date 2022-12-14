# Mars Rover Kata

## Your Task

You’re part of the team that explores Mars by sending remotely controlled vehicles to the surface of the planet. Develop an API that translates the commands sent from earth to instructions that are understood by the rover.

## Requirements
 - The Rover will be connected through a (pseudo)rest-api, security by now is not a problem.
   - `/initialize`: Receives init position in body
   - `/position`: Returns rover current position
   - `/direction`: Returns rover current direction
 - You are given the initial starting point (x,y) of a rover and the direction (N,S,E,W) it is facing.
 - The rover receives a character array of commands.
   - `/move`: Receives an array of moves in the body. Example: ["f", "b", "r", "l"]
 - Implement commands that move the rover forward/backward (f,b).
 - Implement commands that turn the rover left/right (l,r).
 - Implement wrapping at edges. But be careful, planets are spheres. Connect the x edge to the other x edge, so (1,1) for x-1 to (5,1), but connect vertical edges towards themselves in inverted coordinates, so (1,1) for y-1 connects to (5,1).
 - Implement obstacle detection before each move to a new square. If a given sequence of commands encounters an obstacle, the rover moves up to the last possible point, aborts the sequence and reports the obstacle.

## Rules

 - Use Outside-in TDD
 - The point of the exercise is TDD and design not completion
