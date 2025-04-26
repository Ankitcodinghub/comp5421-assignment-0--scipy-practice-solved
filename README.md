# comp5421-assignment-0--scipy-practice-solved
**TO GET THIS SOLUTION VISIT:** [COMP5421 Assignment 0- Scipy Practice Solved](https://www.ankitcodinghub.com/product/comp5421-homework-assignment-0-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;124254&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;COMP5421 Assignment 0- Scipy Practice Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
Scipy Practice

This homework will not be graded. It is meant to provide some Python/Scipy practice exercises to ensure that coding will not be an obstacle for you during this course. However, it IS REQUIRED that you submit an attempt. Please follow the submission instructions at the end of the assignment. This and future assignments will assume that you are using Python 3+ and the latest Scipy libraries (numpy, matplotlib, etc). The recommended approach is to use the Anaconda Python 3 distribution.

1 Color Channel alignment

The easiest way to do this is to exhaustively search over a window of possible displacements for the different channels (you can assume the displacement will be between -30 and 30 pixels). Score the alignment from each possible displacement with some heuristic and choose the best alignment using these scores. You can use the following metrics:

1. Sum of Squared Differences (SSD)

This metric tries to compare the distance between two vectors, hence we can use this to compare image pixel intensity differences. For two vectors u, v of length N, this metric is defined as

N

SSD(u,v) = X(u[i] − v[i])2

i=1 (essentially like the Euclidean distance metric).

2. Normalized Cross Correlation (NCC)

This metric compares normalized unit vectors using a dot product, that is for vectors u,v,

u v

NCC(u,v) = ·

||u|| ||v||

Implement an algorithm which finds the best alignment of the three channels to produce a good

RGB image; it should look something like Figure 2. Try to avoid using for loops when computing

Figure 1: Combining the red, green, and blue channels without shifting

Figure 2: Aligned image

the metrics (SSD or NCC) for a specific offset. Some starter code is given in script1.py and alignChannels.py. Save your result as rgb output.jpg in the results folder.

2 Image warping

We will be writing code that performs affine warping on an image. Code has been provided to get you started. In the following sections you will be adding your own code.

2.1 Example code

The file script2.py contains example code which demonstrates basic image loading and displaying as well as the behavior of an image warping function. Try running script2. You should see something like Figure 3. This script calls the function warp in warpA check.py, which is simply a wrapper for scipy’s own function scipy.ndimage.affine transform.

Figure 3: See script2.py

2.2 Affine warp

You will write your own function in warpA.py, that should give the same output as the function in warpA check.py. First we’ll walk through what you need to know about affine transformations. An affine transform relates two sets of points:

piwarped pisource + t (1)

L

where pisource and piwarped denote the 2D coordinates (e.g., pis = (xis,ysi)T) of the i-th point in the source space and destination (or warped) space respectively, L is a 2×2 matrix representing the linear component, and t is a 2×1 vector representing the translational component of the transform.

To more conveniently represent this transformation, we will use homogeneous coordinates, i.e., pis and piw will now denote the 2D homogeneous coordinates (e.g., pis ≡ (xsi,ysi,1)T), where “≡” denotes equivalence up to scale, and the transform becomes:

!

pid ≡pis (2)

| {z }

A

• Implement a function that warps image im using the affine transform A: warp im = warpA(im, A, output shape)

Inputs: im is a grayscale double typed Numpy matrix of dimensions height × width × , A is

a 3 × 3 non-singular matrix describing the transform (piwarped ≡ Apisource), and output size=[out height,out width]; of the warped output image.

Outputs: warp im of size out size(1) × out size(2) is the warped output image.

The coordinates of the sampled output image points piwarped should be the rectangular range (0,0) to (width −1,height −1) of integer values. The points pisource must be chosen such that their image, Apisource, transforms to this rectangle.

Implementation-wise, this means that we will be looking up the value of each of the destination pixels by sampling the original image at the computed pisource. (Note that if you do it the other way round, i.e., by transforming each pixel in the source image to the destination, you could get “holes” in the destination because the mapping need not be 1 to 1). In general, the transformed values pisource will not lie at integer locations and you will therefore need to choose a sampling scheme; the easiest is nearest-neighbor sampling (something like, round(pisource)). You should be able to implement this without using for loops (one option is to use numpy.meshgrid and Numpy’s multidimensional indexing), although it might be easier to implement it using loops first. Save the resulting image in results/transformed.jpg.

You should check your implementation to make sure it produces the same output as the warp function provided in warpA check.py (for grayscale or RGB images). Obviously the purpose of this exercise is practicing Python/Scipy by implementing your own function without using anything like scipy.ndimage.affine transform.

3 Submission and Deliverables

Please submit a zip file to CASS for this homework of the form &lt;ust-login-id&gt;.zip. Running script1.py and script2.py from within the code/ folder should produce the outputs transformed.jpg, and rgb output.jpg in the results/ folder. You should not include the data/ folder in your submission. An example submission zip file should be:

sigbovik.zip:

• code/

– script1.py

– script2.py

– warpA.py

– warpA check.py

– any other files your code needs to run

• results/

– rgb output.jpg for Question 1

– transformed.jpg for Question 2
