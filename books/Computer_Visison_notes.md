# Affine Transformation

An **affine transformation** is a linear mapping technique used in image processing to perform geometric transformations such as translation, rotation, scaling, and shearing—all in a single operation.

## Mathematical Formulation

The transformation of a point (x, y) to a new point (x', y') is given by:

```
[ x' ]   [a11 a12]   [ x ]   [tx]
[ y' ] = [a21 a22] * [ y ] + [ty]
```

- The **2x2 matrix** handles rotation, scaling, and shearing.
- The **translation vector** (tx, ty) shifts the image.

## Properties

- **Parallel lines remain parallel.**
- **Ratios of distances along parallel lines are preserved.**
- **Straight lines remain straight.**

## Example

Suppose you want to rotate a point by 90° and then translate it by (2, 3):

- **Rotation matrix for 90°:**

```
[ 0  -1 ]
[ 1   0 ]
```

- **Translation vector:** (2, 3)
- **Original point:** (1, 0)

**Calculation:**
- After rotation: (0, 1)
- After translation: (0+2, 1+3) = (2, 4)

## Applications

- Image registration (aligning images)
- Geometric correction
- Mapping between coordinate systems

## Book Reference

- **Book:** Digital Image Processing (4th Edition) by Gonzalez and Woods
- **Chapter:** 2 (Digital Image Fundamentals)
- **Section:** 2.7 (Image Transformations)
- **Pages:** ~85–90 (check your edition’s table of contents for the exact page)

---

**Summary:**  
Affine transformations are essential for manipulating images geometrically, as they combine translation, rotation, scaling, and shearing while preserving straightness and parallelism of lines.
