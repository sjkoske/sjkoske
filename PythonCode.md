## This is some code used to calculate the position of an object given initial position, velocity, acceleration, and time.
~~~
#The beginning of the proogram starts with an infinite while loop.
#This is so that the user can repeat an infinite amount of calculations without the program ending.
#As long as do_calculation is true, the while loop will continue


do_calculation= True
while (do_calculation):


    #Input of the initial position using a while loop. To prevent the program from crashing or outputing a problematic output, we use the 'except' and 'if' functions. 
    while (True):
            try:
                xnaught = float(input("Enter initial position (m): "))
                if (xnaught < 0):
                    print("negative initial positions are not allowed")
                    continue
            except(ValueError):
                print("The value you have entered is invalid. Only numerical values are valid.")
            else:
                break
    print("\nIntitial position is: " +str(xnaught))

   
   
   #Input of the initial velocity usuing the same ideas as before
    while (True):
        try:
            vnaught = float(input("\nEnter initial Velocity (m/s): "))
            if (vnaught < 0):
                print("negative initial velocities are not allowed")
                continue
        except(ValueError):
                print("The value you have entered is invalid. Only numerical values are valid.")
        else:
            break
    print("\nInitial velocity is: " +str(vnaught))
    
    
    #Input of the initial acceleration
    while (True):
        try:
            anaught= float(input("\nEnter the initial acceleration (m/s^2): "))
            if (anaught < 0):
                print("negative initial accelerations are not allowed")
                continue
        except(ValueError):
                print("The value you have entered is invalid. Only numerical values are allowed.")
        else:
            break
    print("\nInitial acceleration is: " +str(anaught))


    #Input of the time over which object travels
    while (True):
        try:
            t= float(input("\nEnter the time over which the object moves (s): "))
            if (t < 0):
                print("negative time is not allowed")
                continue
        except(ValueError):
            print("The value you have entered is invalid. Only numerical values are allowed.")
        else:
            break
    print("\nTime is: " +str(t)+'\n')


    #Calculation using the equation
    xf= xnaught + (vnaught*t) + ((0.5*anaught)*(t**2))
    print('The final position of the object is: ' + str(xf)+' m/s\n.')


    #This sets the condition of the while loop. If the user inputs 'n' then the infinite while loop at the beginning of the program is now 'False' causing the program to end. 
    another_calculation = input("Do you want to perform another calcuation? (y/n): ")
    if (another_calculation != "y"):
        do_calculation = False
   ~~~
   [take me back to home](
