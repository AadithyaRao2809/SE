### Vectors and points

- Point + Vector = New Point
- Vector +Vector = new vector
- Points exist in space
- Coordinate system gives a number


#### Spaces
- **vector**
	consists of vectors and scalars
	
- **affine**
	includes points to vector space
	vector point addition can now be done
	Addition of points not defined
	Multiplication of a point with a scalar
	
- **euclidean**
	adds a measure of size and distance to vector space


#### ADT

sees points,vectors and scalars as ADT's
Give a datatype and define operations

for affine:
![](../Attachments/Unit%202-20230926.png)
These are not arbitrary points
constrained by $\alpha_1$ & $\alpha_2$
![](../Attachments/Unit%202-20230926-1.png)

#### Convex Object

All interior angles <180$\degree$
![](../Attachments/Unit%202-20230926-2.png)

Smallest dimension convex object that contains a set of points->convex hull

##### Where is it used
- geometry
- robotic path planning
- Computer graphics
	- Collision detection
	- Shadows and lighting




*Grahams Algo for convex full*
![](../Attachments/Unit%202-20230926-3.png)
If another point was at 0 level,we give priority to the leftmost point

### Barycentric Coordinate

Representation of a point wrt other points
![](../Attachments/Unit%202-20230926-4.png)


### Coordinate System And Frames

![](../Attachments/Unit%202-20230926-5.png)
![[../Attachments/Unit 2 2023-09-26 13.36.32.excalidraw]]
We can represent any vector(magnitude and direction), but we still face the problem of representing a point(fixed position)
![](../Attachments/Unit%202-20230926-6.png)

**INSERT AFFINE SPACE**
Choose origin $p_0$ and we attach basis vectors there->called a frame
![](../Attachments/Unit%202-20230926-7.png)
$P_0$ is origin

![](../Attachments/Unit%202-20230926-8.png)
euclidian adds a distance tuple-special space where vectors represent points in n dimensional real space

#### Coordinates in OpenGL
1) Object/Model
2) World 
3) Camera
4) Clip
5) Normalized Device 
6) Window/Screen

#### Change of coordinate systems
![](../Attachments/Unit%202-20230926-9.png)
![[../Attachments/Unit 2 2023-09-26 13.55.06.excalidraw]]
![](../Attachments/Unit%202-20230926-10.png)
![](../Attachments/Unit%202-20230926-11.png)
![](../Attachments/Unit%202-20230926-12.png)

- Point: 
	![](../Attachments/Unit%202-20230926-13.png)
- Vector will have last column as 0


#### Updated Transformation matrix

**But basis vector maps to a real point**
##### Homogenous Coordinates
![](../Attachments/Unit%202-20230926-14.png)
![](../Attachments/Unit%202-20230926-15.png)
In the above you are changing basis
lets take rotations around Z for example, 
![](../Attachments/Unit%202-20230926-19.png)
![[../Attachments/Unit 2 2023-09-26 17.00.32.excalidraw]]
![](../Attachments/Unit%202-20230926-20.png)
![](../Attachments/Unit%202-20230926-21.png)

#### Rigid Body Transformation

Include rotations and transformations
Sheer not included


### Quaternions
![](../Attachments/Unit%202-20230926-16.png)
![](../Attachments/Unit%202-20230926-17.png)
u is unit so sqrt(u1+u2+u3)=1
![](../Attachments/Pasted%20image%2020230926164414.png)
![](../Attachments/Unit%202-20230926-18.png)
$v_1$ stays there while other two rotate by 2$\phi$ around $i$




