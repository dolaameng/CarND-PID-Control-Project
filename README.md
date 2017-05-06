# CarND-Controls-PID
Self-Driving Car Engineer Nanodegree Program


## Build & Run
See [original README from course](file://ORIGINAL_README.md)

## Explaination of Parameter Choice for PID
Starting from the values given in the class, which is 0.2, 0.004, 3.

Based on visual observations in simulations:
- 1. `P` controls how fast the syesm reacts to error. Having a high P means you
can even drive in a wiggly track. However, high P tends to make oscillations worse, specially when there is "noise" in driving. 
- 2. `I` helps when the car has deviated a lot - `I` control will eventually bring it back. However, it can amplify the oscillations because the error builds up.
- 3. `D` helps reduce the oscillations caused by `P` and `I`. However if `D` is too big, it will make the car very rigid (e.g., hard to control when turning).

So in general, 
- Choose a reasonable `P` first based on the complexity of track and car speed.
- Starting from a small `I`. If the driving is not good enough for some segments, increase the `I` value until it satisfies. 
- Use `D` to ahieve a balance between oscillation and driving smoothness.

## Results

### Driving at low speed for comfortability
- [![Driving at low speed for comfortability](https://img.youtube.com/vi/L06mBe9CKSM/0.jpg)](https://www.youtube.com/watch?v=L06mBe9CKSM)

### Driving at higher speed
- [![Driving at higher speed](https://img.youtube.com/vi/nqcz3rfTuBk/0.jpg)](https://www.youtube.com/watch?v=nqcz3rfTuBk)