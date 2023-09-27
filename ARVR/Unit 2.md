### Vectors and points

- Point + Vector = New Point
- Vector +Vector = new vector
- Points exist in space
- Coordinate system gives a number


### Spaces
- **vector**
	consists of vectors and scalars
	
- **affine**
	includes points to vector space
	vector point addition can now be done
	Addition of points not defined
	Multiplication of a point with a scalar
	
- **euclidean**
	adds a measure of size and distance to vector space

#### Affine
for affine:
![](../Attachments/Unit%202-20230926.png)
These are not arbitrary points
constrained by $\alpha_1$ & $\alpha_2$
![](../Attachments/Unit%202-20230926-1.png)


### ADT

sees points,vectors and scalars as ADT's
Give a datatype and define operations


### Convex Object

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
Choose origin $p_0$ and weattach basis vectors there->called a frame
![](../Attachments/Unit%202-20230926-7.png)
$P_0$ is origin

![](../Attachments/Unit%202-20230926-8.png)
euclidian adds a distance tuple-special space where vectors represent points in n dimensional real space


#### Coordinate System in openGL
##### Object/Local Coordinate System (Model Space)

- **Purpose:** Local coordinate system for individual objects.
- **Origin:** Typically at the object's center.
- **Transformation:** Object-specific transformations (e.g., translation, rotation, scaling) are applied here.
- **Example:** Car components are positioned and oriented relative to the car's local coordinate system.

##### World Coordinate System (World Space)

- **Purpose:** Global reference frame for the entire scene.
- **Origin:** Arbitrary, often set at a convenient location.
- **Transformation:** Objects are placed and oriented within the world coordinate system.
- **Example:** Multiple objects (e.g., car, building, tree) are positioned and oriented in the world coordinate system.

##### Eye Space (Camera Space)

- **Purpose:** Represents the view from the camera's perspective.
- **Origin:** Typically at the camera's position (viewer's eye).
- **Transformation:** View matrix maps objects from world space to eye space for rendering.
- **Example:** A camera looks at a car, transforming its position and orientation into eye space.

##### Clip Space

- **Purpose:** Homogeneous coordinate system for clipping and perspective division.
- **Origin:** At the frustum's center defined by the camera.
- **Transformation:** Projection matrix maps objects from eye space to clip space. Clipping and perspective division occur here.
- **Example:** Objects outside the camera's frustum are clipped, and perspective effects are applied.

##### Normalized Device Coordinate (NDC) Space

- **Purpose:** Coordinates after perspective division and normalization.
- **Origin:** Typically at the screen's center.
- **Range:** Coordinates range from -1 to 1 along each axis.
- **Transformation:** Mapped from clip space; further transformations for screen mapping.
- **Example:** Coordinates are normalized for final screen mapping.

##### Screen Space

- **Purpose:** Represents 2D screen or viewport coordinates.
- **Origin:** Typically at the top-left screen corner.
- **Transformation:** Viewport transformation maps NDC coordinates to screen pixels.
- **Example:** Objects are in pixel coordinates for direct screen display.


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
#### Homogenous Coordinates
![](../Attachments/Unit%202-20230926-14.png)
![](../Attachments/Unit%202-20230926-15.png)
![](../Attachments/Unit%202-20230926-19.png)
![[../Attachments/Unit 2 2023-09-26 17.00.32.excalidraw]]
![](../Attachments/Unit%202-20230926-20.png)
![](../Attachments/Unit%202-20230926-21.png)

#### Rigid Body Transformation

Include rotations and transformations
Sheer not included


### Quaternions
![](../Attachments/Unit%202-20230926-26.png)
![](../Attachments/Unit%202-20230926-27.png)
![](../Attachments/Unit%202-20230926-28.png)
![](../Attachments/Unit%202-20230926-16.png)
![](../Attachments/Unit%202-20230926-17.png)
u is unit so sqrt(u1+u2+u3)=1
![](../Attachments/Pasted%20image%2020230926164414.png)
![](../Attachments/Unit%202-20230926-18.png)
$v_1$ stays there while other two rotate by 2$\phi$ around $i$
![](../Attachments/Unit%202-20230926-22.png)
![](../Attachments/Unit%202-20230926-23.png)
![](../Attachments/Unit%202-20230926-24.png)
![[../Attachments/Unit 2 2023-09-26 20.48.34.excalidraw]]





