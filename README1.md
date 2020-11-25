# Coolguy_basic_extension

Coolguy basic extension for Makecode. It's micro:bit extension board, which include basic functionalities like battery module, two DC motor drivers and 5V IO interfaces. What's more the inteface is RJ11 based, it's easy to connect by users. 

## Feature

- Onboard battery source (powered by 3.7V rechargeable battery)
- Drive two motors simultaneously (motor interface A and B)
- Two IIC communication interfaces (serial interface A and B)
- Three dual IO interfaces（interface P1, P2, and P16）
- A multiplexing IO interface（interface P0）

## Link to product page

http://www.coolguyrobot.com/down/Microbit%E6%89%A9%E5%B1%95%E6%9D%BF%E5%8F%8AMakecode%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E.pd

## Hardware Preview

- ### front

![Product](https://user-images.githubusercontent.com/45141802/99250737-22689380-2847-11eb-817a-30b43995aa79.png)

![back view](https://user-images.githubusercontent.com/45141802/99250756-2b596500-2847-11eb-9a7c-53202cc0e2c8.png)

## Software Preview

### Motor

Using the blocks under ‘Motors’ in Coolguy_basic is the simplest way to drive a motor. In that case, you may specify the port forward or reversal separately. You may also control the little car to move forward, move backward, or turn in the speed level from 0 to 255. The two motors will both drive according to the selected speed level and direction. 

`// Move forward at speed 60 forever`

![basic_motor1](https://user-images.githubusercontent.com/45141802/99250784-344a3680-2847-11eb-9a27-82cbf24e136a.png)

`// Move backward at speed 100 forever`

![basic_motor2](https://user-images.githubusercontent.com/45141802/99250795-37452700-2847-11eb-8011-a21f6127ee3e.png)

#### Stopping

The motor will stop when its speed is set to zero. However, we can also use the motor itself to generate reverse current to brake faster, which helps to perform more precise operations. Use the command `exter_motor_stop(...)` to stop braking or coast to stop.

`# rapidly brake`

![basic_motor3](https://user-images.githubusercontent.com/45141802/99250800-37ddbd80-2847-11eb-9cea-09c1a93a2374.png)

#### Drive motors separately

If you want `bitbot.move(...)` to perform finer control on a single motor, please use to drive each motor forward or backward. You may specify the speed level from 0 to 255, and you can select forward and reverse. If the rotation speed of the left motor is slower than the rotation speed of the right motor, the robot will rotate to the left.

`// Drive one motors forward at speed 60 `

![basic_motor4](https://user-images.githubusercontent.com/45141802/99250802-38765400-2847-11eb-8041-3e9386f3a75c.png)

`// Drive left motor in reverse at speed 30 `

![basic_motor5](https://user-images.githubusercontent.com/45141802/99250804-390eea80-2847-11eb-89fe-d65580e6b6d0.png)

`// Drive forward in a leftward curve `

![basic_motor6](https://user-images.githubusercontent.com/45141802/99250807-39a78100-2847-11eb-9053-808804aa81c8.png)

### Beeper

Connect the beeper with analog interface P0, and then the beeper module is available.

`// Buzz for 100 ms `

![basic_beeper](https://user-images.githubusercontent.com/45141802/99250821-40ce8f00-2847-11eb-85a6-4ced1faaf618.png)

### Display digits using the digital tube

A digital tube is provided, which can be used to display expected digits using function `Segment_Init(...)`.

`// The digital tube shows the number 8 `

![basic_segment](https://user-images.githubusercontent.com/45141802/99251100-b9355000-2847-11eb-8e5b-76a0fa1148ca.png)

### Ultrasonic distance measure

The extension board provides an ultrasonic sensor so that the distance between the sensor and the barrier can be measured using the function `ultrasonic_get(..)`. 

`// Read Ultrasonic values `

![basic_ultrasonic](https://user-images.githubusercontent.com/45141802/99251257-fc8fbe80-2847-11eb-8a00-5e9ed648f146.png)

### RGB module

RGB module makes it possible to select color and brightness via RGB value. The brightness level is up to 255 with a default value of 120. Do not look directly when the brightness level is high, otherwise, eyes would be damaged. 

`// Set brightness of RGB to 100 set color blue `

![basic_RGB](https://user-images.githubusercontent.com/45141802/99251455-57c1b100-2848-11eb-8200-9699a90b49fb.png)

### Infrared remote control

The infrared remote-control module should have cooperated with the Coolguy remote controller and the infrared receiver. There are 8 channels to be selected, which can prevent channel conflicts. You may use the infrared remote controller to control the little car to move forward or backward.

`//Control the little car to move using a remote controller`

![basic_remote](https://user-images.githubusercontent.com/45141802/99251575-86d82280-2848-11eb-92df-ea432c18687d.png)

## License

MIT

## Supported targets

* for PXT/microbit (The metadata above is needed for package search.)

