# Communicating between Methods and Modules

Example: Converting miles/hour to kilometers/hour

ConvertMPH2KMH
    prompt user "Enter miles/hour"
    get milesPerHour
    result = calculateKilometersPerHour(milesPerHour)
    display result
    END
calculateKilometersPerHour(milesPerHour)
    return milesPerHour * 0.62137119
    
    