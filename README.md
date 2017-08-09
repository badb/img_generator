## TODO:
1) Find the threshold value for Verified/Unknown/Wrong state as a function of img resolution an haltspp.
2) Do the same using cropwindow (parameter in scene_configfile.lxs) for:

    a) calculating the distance between imgs.
    What is the minimal (speed vs accuracy) resolution for calculating distance between imgs?

    b) rendering 'cropped' reference img (speed vs accuracy) - it turns out that imgs produced in this way are slightly darker.
    Can we find a reasonable threshold value despite of it?

## Dependencies:
1) Two external Python packages, pyssim and OpenEXR.
    Pyssim may require Numpy+mkl (make sure this version is installed), however it shall go smoothly:
    
    ```bash
        pip3 install pyssim
    ```
    
    Installing vendor's OpenEXR on Python3 can be problematic. You may use our package:
    
    ```bash
        git clone https://github.com/golemfactory/golem.wiki.git
    ``` 
    Go to the wheels folder to find appropiate OpenEXR-yourOS.whl
    
    ```bash
        pip3 install OpenEXR-1.3.0-cp35-cp35m-manylinux1_x86_64.whl 
    ```      
    
2) Install Luxrender standalone (http://www.luxrender.net/en_GB/download) and add it to PATH, so that command "luxconsole" is available in your system.
3) Install Blender  (http://www.blender.org) and add it to PATH, so that command "blender" is available in your system.


### Notes:
Might be useful:

https://en.wikipedia.org/wiki/Mahalanobis_distance

https://en.wikipedia.org/wiki/Multivariate_normal_distribution

Keep in mind that Blender and Lux has different corner marked as (0, 0) when
you are using crop option.
