
# Gesture Navigation

A brief description of what this project does and who 
Flutter Package for Gesture-Based Navigation

gesture_navigation enhances user experience by providing gesture-based navigation and controls for Flutter apps. This package supports:

✔ Edge Swipe Gestures (Left & Right)\
✔ Pinch-to-Zoom with Panning & Rotation\
✔ Drag & Drop Reordering\
✔ Swipe Navigation between Pages\
✔ Modal Control with Swipe Up/Down to Dismiss\
✔ Customizable Gesture Sensitivity & Feedback

This package enables smooth and intuitive interactions, making your app more engaging.

Features:\
✅ Edge Gestures – Detect left and right edge swipes.\
✅ Pinch Zoom – Enables zoom, panning, and rotation on widgets.\
✅ Reorderable Drag & Drop List – Users can reorder items seamlessly.\
✅ Swipe Navigation – Swipe between pages with smooth transitions.\
✅ Modal Swipe Control – Swipe up/down to open/dismiss modals.\
✅ Customizable Feedback – Toggle haptic feedback and snackbar notifications.\
✅ Optimized Performance – Built for responsiveness & efficiency.



## Installation:
To use this package, add the following dependency to your pubspec.yaml:
```
dependencies:
  gesture_navigation: ^0.0.1
```


https://github.com/user-attachments/assets/9b25aa59-8df4-40cc-b725-560ec5fd7866


## Edge Gesture (Left & Right Swipe):
```
EdgeGesture(
        onSwipeLeftEdge: () {
          ScaffoldMessenger.of(context).showSnackBar(
            SnackBar(content: Text("Swiped from Left Edge!")),
          );
        },
        onSwipeRightEdge: () {
          ScaffoldMessenger.of(context).showSnackBar(
            SnackBar(content: Text("Swiped from Right Edge!")),
          );
        },
        child: Center(child: Text("Swipe from the left or right edge")),
      ),
```

## Pinch-to-Zoom with Panning & Rotation:
```
PinchZoom(
          allowRotation: true,
          child: ClipRRect(
            borderRadius: BorderRadius.circular(15),
            child: Image.asset('assets/sample_image.jpg', width: 250),
          ),
        ),

```

## Drag & Drop Reordering:
```
DragReorder(
        items: items,
        onReorder: updateOrder,
      ),

Swipe Navigation:
SwipeNavigation(
      pages: [
        PageScreen(title: "Page 1"),
        PageScreen(title: "Page 2"),
        PageScreen(title: "Page 3"),
      ],
    );
```

## Modal Swipe Control:
```

ElevatedButton(
          onPressed: () => showModalBottomSheet(
            context: context,
            isDismissible: false,
            builder: (_) => ModalControl(
              onSwipeDown: () => Navigator.pop(context),
              child: Container(
                height: 300,
                color: Colors.white,
                alignment: Alignment.center,
                child: Text("Swipe Down to Close", style: TextStyle(fontSize: 18)),
              ),
            ),
          ),
          child: Text("Open Modal"),
        ),
```
