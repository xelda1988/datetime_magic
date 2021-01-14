# Datetime Magic

Semi-automatically converts datetime strings into a preferred datetime format.

The core idea is that this library
clusters from a list of datetime format strings 
each unique input format and detects the corresponding format

you can then manually correct those detections by correcting certain ids
manually and correcting the detected formats generically.

    import datetime_magic as dm
    x = ['7/31/2018', 'Sept 15 2020 4:00:15']
    dm.detect(x)
    print(dm.detections)
    
    >> _format_clusters: {0:'%d/%m%/%y',1:'%b %d %y %h:%mm:%ss'}
    >> _example_mappings: {0:[0], 1:[1]}
    
