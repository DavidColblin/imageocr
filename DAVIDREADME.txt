This is a PHPOCR...
i wanted to use it as an OMR where it will learn about shapes instead of characters.

example.php is the learning phase, it scans the image and stores the parameters in storage directory.
example_1.php uses the parameters in storage directory to deduct which image ressembles the most.

the problem with the class is that it recognizes only shapes when they are alone and clear in the image...
as you can see in marker_test1.png, the test run will return too much error and not recognise it.

possible idea 1: use a stronger threshold with help of PHP GD (http://php.net/manual/en/book.image.php) and try to isolate the marker to get a 'clearer' image. the problem is that the marker itself can be erased as well in the process.

possible idea 2: if the marker width and height is 100x100 pixels, we can isolate each 100x100 squares in the image and analyse each of them until reaching the marker. the problem is that it is very CPU consuming and takes a lot of time. 


Resolution: a collegue already knows a lot about image recognition on Python, so, i'll it up to her.