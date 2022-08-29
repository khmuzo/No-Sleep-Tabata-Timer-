import time

def tabata_timer():
    round = 1 # all 4 exercises = 1 round
    set = 1 # 4 rounds = 1 set
    timework = 30 # time working
    timerest = 30 # time resting
    duration = timework + timerest # total time for each exercise
    while set <= 4:
        print("Set", set)
        round = 0 # resets the exercise list for each set
        exercisetext = ""
        while round <= 3:
            if round == 0:
                exercisetext= "Push Up"
            if round == 1:
                exercisetext= "Squat"
            if round == 2:
                exercisetext= "KB Swing"
            if round == 3:
                exercisetext= "Lunge"
            print("Exercise #",int(round)+1 ,": ", exercisetext) # example "Exercise #1: Push Ups"
            duration = timework + timerest #resets the timer for each exercise
            choice1timer = time.time()  # get start time in seconds
            work = choice1timer + duration  # work = the time in seconds that the workout will end
            clock = str(int(choice1timer)) #convert seconds to string so it can be turned into a list then a shorter number
            clock = clock[-3:]  # use the last 3 digits of the time
            timer2 = int(clock) + int(duration)  # time in seconds that the workout will end (last 3 digits)
            timeleft = int(work) - int(clock)
            while timeleft > 0:
                choice2timer = time.time()
                clock = str(int(choice2timer))
                clock = clock[-3:] # get the time as a 3 digit non-moving number
                # print("Time: ", choice1timer, "Clock:", clock)
                work = choice1timer + duration
                work = str(int(work))
                work = work[-3:]
                # print("Work:",work, "Clock:",clock)
                timeleft = int(work) - int(clock)
                text = ""
                timer = ""
                if timeleft >= timerest:
                    text = "Work"
                    timer = timeleft - timerest
                if timeleft <= timerest:
                    text = "Rest"
                    timer = timeleft

                print("Set:",set,"Exercise ",int(round)+1 ,": ", exercisetext,"Activity:",text,"Time Left:",timer)
            round += 1
        set += 1

tabata_timer()
