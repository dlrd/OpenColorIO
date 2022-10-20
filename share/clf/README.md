<!-- SPDX-License-Identifier: CC-BY-4.0 -->
<!-- Copyright Contributors to the OpenColorIO Project. -->

The ACES project has had a working group focused on building a package of resources to aid in 
the development of implementations and integrations of the Academy/ASC Common LUT Format (CLF).  
These resources include the following:

- An implementation guide
- A collection of CLF test files
- A source target image and reference images generated by processing it through the test CLFs

The website for the CLF Implementation working group is here:

[https://paper.dropbox.com/doc/CLF-Implementation-Virtual-Working-Group--BYL3SxNbCAEOmKl1Sd6TkNM5AQ-cGWer0ASqKzhIzG00FNpS](url)

Because OpenColorIO is open source and has a very complete CLF implementation, it has been used 
in the generation of the test kit.  For example, the recommended collection of CLF test files 
consists of files in the OCIO unit tests, in the directory:  tests/data/files/clf/*

Furthermore, the Python scripts and image adjacent to this README may be used as follows:


### CLF_testImage.exr

This is the source target image.  It samples the full domain of half-float values.  More 
information about this target is available at:  

[https://github.com/alexfry/CLFTestImage](url)


### process_clf_test_frames.py

This script will use OCIO to process the source target image through the collection of CLF test 
files to produce the reference image set.


### compare_clf_test_frames.py

This script will use OpenImageIO to compare the reference images to a set of images processed 
by another implementation and compare them to see if they are within the tolerance specified in 
the CLF Implementation Guide.


For more information, please refer to the CLF Implementation Guide and the usage instructions 
in the individual scripts.