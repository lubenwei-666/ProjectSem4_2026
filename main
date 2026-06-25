from microbit import *
import tinybit

# Predefined custom speed parameters for user speed adjustment (Sprint1)
FAST_SPEED = 200
SLOW_SPEED = 90

# Basic forward, backward and stop movement function
def basic_movement():
    # Run slowly for 2 seconds
    tinybit.CarCtrlSpeed(tinybit.CarState.Car_Run, SLOW_SPEED)
    sleep(2000)
    # Run quickly for 2 seconds
    tinybit.CarCtrlSpeed(tinybit.CarState.Car_Run, FAST_SPEED)
    sleep(2000)
    # Reverse at low speed
    tinybit.CarCtrlSpeed(tinybit.CarState.Car_Back, SLOW_SPEED)
    sleep(1500)
    # Stop all motors
    tinybit.CarCtrl(tinybit.CarState.Car_Stop)
    sleep(1000)

# Left and right directional control function (Sprint2, mobile APP compatible logic)
def direction_control():
    # Turn left for 1 second
    tinybit.CarCtrlSpeed(tinybit.CarState.Car_Left, FAST_SPEED)
    sleep(1000)
    # Turn right for 1 second
    tinybit.CarCtrlSpeed(tinybit.CarState.Car_Right, FAST_SPEED)
    sleep(1000)
    tinybit.CarCtrl(tinybit.CarState.Car_Stop)
    sleep(1000)

# User-defined rectangular automatic driving path (Sprint3 core function)
def predefined_path():
    # Complete four sides of a rectangle
    for count in range(4):
        tinybit.CarCtrlSpeed(tinybit.CarState.Car_Run, FAST_SPEED)
        sleep(2400)
        tinybit.CarCtrlSpeed(tinybit.CarState.Car_Right, FAST_SPEED)
        sleep(920)
    tinybit.CarCtrl(tinybit.CarState.Car_Stop)

# Main program entry, execute all functions sequentially after power on
basic_movement()
direction_control()
predefined_path()
