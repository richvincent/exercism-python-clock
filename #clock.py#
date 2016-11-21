

class Clock:
    def __init__(self,hoursInput,minutesInput):
        """
        Class initiation takes two inputs hours and minutes.
        These two inputs are used to calculate the clock time.
        """
        self.hoursInput = hoursInput
        self.minutesInput = minutesInput
        self.calculate(hoursInput, minutesInput)

    def add(self, additionalTime):
        self.minutesInput += additionalTime
        return(self.calculate(self.hoursInput, self.minutesInput))

    def calculate(self,hoursInput,minutesInput):
        if isinstance(hoursInput,int) and isinstance(minutesInput,int):

            displayHours = str((hoursInput + minutesInput//60)%24)

            if len(displayHours) == 1:
                displayHours = "0" + displayHours
            displayMinutes = str(minutesInput%60)

            if len(displayMinutes) == 1:
                displayMinutes = "0" + displayMinutes
            return('{}:{}'.format(displayHours,displayMinutes))

    def __str__(self):
        return(self.calculate(self.hoursInput, self.minutesInput))

    def __eq__(self, other):
        if isinstance(other, self.__class__):
            return self.__dict__ == other.__dict__
        else:
            return False

    def __ne__(self, other):
        return not self.__eq__(other)
