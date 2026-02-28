#  Starlight UI (Kotlin)

A lightweight, expressive **declarative UI + animation DSL for Android (View-based)** — built to create beautiful layouts with less boilerplate and more readability.

---

##  Features

*  Declarative UI components (`SLColumn`, `SLText`, `SLBtn`, etc.)
*  Powerful styling system via `slStyle { }`
*  Smooth animations via `slAnimate { }`
*  No XML required
*  Flexbox-inspired layout system
*  Clean and readable Kotlin DSL

---

##  Installation

### Maven (Recommended)

```gradle
implementation "com.starlightlang:starlight:1.0.0"
```

---

##  Quick Start

```kotlin
val root = SLColumn {
    slStyle {
        width = MATCH_PARENT
        height = MATCH_PARENT
        padding = 32
        justifyContent = SLStyle.JustifyContent.CENTER
        alignItems = SLStyle.AlignItems.CENTER
    }
}

val text = SLText("Hello Starlight ") {
    slStyle {
        textSize = 22f
        bold = true
    }
}

root.addSL(text)
setContentView(root)
```

---

##  Styling System (`slStyle`)

Fully customizable styling inspired by CSS/Flexbox.

```kotlin
slStyle {
    width = MATCH_PARENT
    height = WRAP_CONTENT

    padding = 16
    marginBottom = 12

    backgroundColor = Color.WHITE
    cornerRadius = 20f
    elevation = 8f

    textSize = 18f
    textColor = Color.BLACK
    bold = true
}
```

---

##  Animations (`slAnimate`)

Simple, powerful animations without XML.

```kotlin
view.slAnimate {
    duration = 500
    alpha = 1f
    translationY = 0f
    interpolator = DecelerateInterpolator()
}
```

---

##  Built-in Animation Helpers

```kotlin
view.fadeIn()
view.fadeOut()
view.scaleIn()
view.scaleOut()
view.slideUp()
view.bounce()
view.pulse()
view.shake()
view.fadeSlideIn()
view.rotateScale()
```

---

##  Advanced Animation

```kotlin
view.slAnimate {
    duration = 600
    scale = 1.2f
    translateYBy = -50f
    repeatCount = 1
    repeatMode = ValueAnimator.REVERSE
}
```

---

##  Components

| Component  | Description       |
| ---------- | ----------------- |
| `SLColumn` | Vertical layout   |
| `SLRow`    | Horizontal layout |
| `SLText`   | TextView wrapper  |
| `SLBtn`    | Button component  |

---

##  Why Starlight?

*  Cleaner than XML
*  Faster UI development
*  Centralized styling
*  Built-in animation engine
*  Easy to learn, powerful to use

---

##  Project Structure

```
com.starlightlang.lib
├── SLStyle.kt
├── SLAnimation.kt
├── Starlight.kt
```

---

##  Roadmap

* [ ] Compose-like state system
* [ ] More UI components
* [ ] Gesture support
* [ ] Theme system
* [ ] Recycler DSL

---

##  Contributing

Contributions are welcome!

1. Fork repository
2. Create a new branch
3. Submit a pull request 

---

##  License

MIT License

---

##  Author

Developed by **Dominex Macedon**

