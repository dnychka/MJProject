




<h2>Digital Elevations and Digital Orthophoto fields for The Mary
Jane Ski Resort</h1>
<p>
</p><h2>  <a href="https:/dnychka.github.io"> Doug Nychka </a>   <p></p> </h2>

<img style="width: 232px; height: 137px;" src="./Data/MJlogo.jpg" alt="" align="top"><img style="width: 253px; height: 203px;" src="./Data/DSCN0879.jpg" alt=""><br>


These data form the basis for a extended example using the
fields package for fitting and manipulating curves and surfaces. Refer to the<a href="./Data/MJposter.pdf"> poster</a>, presented at the
Joint Statistical Meetings of the American Statistical Association 2007 for more details on the statistics. In particular this is the first substantial application of the <a href="https:/guthub.NCAR/LatticeKrig"> LatticeKrig </a>
R package.  The
three data components for this example are georeferenced from the
WinterPark Mary Jane Ski resort in Colorado and centered around the
Super Gauge lift and Riflesight notch ski trial. <br>


<h2> Mary Jane Project</h2>
The Mary Jane Project (MJP)
is a web based guide for the primary ungroomed trails
at Winter Park/Mary Jane ski resort. This page provides some
quantitative analysis of one run that is part of the MJP. <br>


We would like to acknowledge Allie Nychka from MJProject for sharing her
broad knowledge on the ski area.
<br>
</p>

<a href="http://www.image.ucar.edu/Data/MJProject/narrative.html"> 
<h2> Narrative </h2>
</a>
<ul>
  <li><a href="narrative.html#motivation">Motivation</a>
  </li>
  <li><a href="narrative.html#guide">Guide to the run</a>
  </li>
  <li>  <a href="narrative.html#work">Some other work</a>
  </li>
</ul>


<h2> Data sets</h2>

The R datasets and supporting functions are contained in the R binary
format file <a href="./Data/RifleSight.rda"> <b>MaryJane.rda</b> 
</a>. 
(just download this file -- don't let your browser try to display it!)


  </p><li>Digitial elevation model (DEM) on a 146X196 grid.
Elevations in meters with an approximate grid spacing of 10m.
 R data set name is <span style="font-weight: bold;">RifleDEM.
    </span> This image  was extracted
 from a  larger  DEM  that
 covers  Winter  Park and  Berthoud
 Pass. </li>




  <li>
    
  Digital orthophoto on a 1155X2003
grid.  Range of grey levels is 5 to 254. R dataset name is <span style="font-weight: bold;">RifleImage</span>.
 Detailed <a href="./Data/MJProject/photometa.html"> meta
data </a> provided with the download
describes the process and accuracy of
this image. The raw image is in
tiff format. This was converted to pnm format and
then read into R using the <span style="font-style: italic;">pixmap</span>
package.  <span style="text-decoration: underline;"></span>
    <b>RifleE</b> is a simple bilinear interpolation of the DEM elevations
to  the finer image grid created in fields using <b> interp.surface.grid</b>
    </p>
  </li>

  <li>
    <div style="text-align: justify;">
    <p>Riflesight trail. Using the <span style="font-weight: bold; font-style: italic;">locator </span>function
a skiing run  was input beginning at the top of the Super gauge
lift, dropping down Sluice Box (aka Juice Box by R. Lund), continuing under the lift to
      Riflesight, emptying out on Feebleminded to 
 finish at Super Gauge lift.  <span style="font-weight: bold;">RifleI</span> is matrixwith
400 lon/lat locations describing the run and rifle.trail.elev are the
interpolated elevations in meters. See the
 <a href="./Data/MJTrailMap.jpg">Trail Map</a> for what skiers
typically use to navigate. </p>

   
  </li>
</ul>

<p>
Both image datasets were obtained through the USGS seamless data
distribution service. These images are in standard R image list format with
components  <span style="font-weight: bold;">x</span> 
the grid values for longitude,  <span style="font-weight: bold;">y</span> the grid for
latitudes and <span style="font-weight: bold;">z </span>a
matrix of values. <br>
</p><p>
Additional components are<br>
</p><ul>
  <li><span style="font-weight: bold;"></span>
  <span style="font-weight: bold;"></span>
  <span style="font-weight: bold;">two.colors, MJ.colors: </span>
   Useful
color table functions for converting grey scale from white to
green. </li>


  <li><span style="font-weight: bold;">fig3.RifleSight:</span>
       R function  for  perspective figure
       of image with ski run superimposed.</li>


  <li><span style="font-weight: bold;">trail.degrees:
    </span>Estimated slope in degrees of the run based on the
                   DEM's and spatial analysis.</li>


  <li><span style="font-weight: bold;">fig4.RifleSight:
    </span>R function  for image plot of photo with
slopes of run and elevation contours</li>


  <li><span style="font-weight: bold;">fields.style</span>:
Some default sizes for characters and colors for the figures</li>

</ul>

|fig3.RifleSight|fig4.RifleSight|
|---------------------------------|------------------------------|
|<img style="width: 240px; height: 240px;" alt="" src="./Data/rifle.png"> | <img style="width: 210px; height: 280px;" alt="" src="./Data/slopeimage2.png"> |
| | (Ski run from  Lower left to upper right)|

  <h2>
<a href="./Rcode.html">More detailed data analysis including Kriging using R  and
fields</a>
</h2>



<h2>DISCLAIMER:</h2>
<p>The data sets, software and related content in and linked to these pages
   are intended for scientific and mathematical research. The authors do not
   guarantee the correctness of the data, software or companion text.
  
