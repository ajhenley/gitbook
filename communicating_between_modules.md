# Communicating between Methods and Modules
Often you will need to send data to your modules as an input. You may then receive that data back as the output and all the processing steps would occur within the module.

You can accomplish this by passing parameters and returning values.


Example: Converting miles/hour to kilometers/hour

ConvertMPH2KMH
    prompt user "Enter miles/hour"
    get milesPerHour
    result = calculateKilometersPerHour(milesPerHour)
    display result
    END
calculateKilometersPerHour(milesPerHour)
    kph = milesPerHour * 0.62137119
    return kph
    
    