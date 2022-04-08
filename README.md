# Build-Your-First-Android-App-in-Kotlin
Learn to write Android app in Kotlin,. in order to support other personal project portfolios.

### VB
How to create a project in Android Studio.

How to create an emulated Android device.

How to run your app on the emulator.

How to run your app on your own physical device.

### V0
How to use the layout editor.

  - Each layout has a root view, which is a view group of other views.

How to set property values.

  - Set string properties under common attributes.

  - All views must have layout_height and layout_width properties (e.g. match_parent, match_constraint, wrap_content)

How to add string resources.

  - String resource is a separate file containing string values identified by tags. Simplify translation to other languages, since no need to mess with the actual code.

  =Advantage of using resources: define the same values used in multiple places

How to add color resources

```
<color Name="ColorName">#AARRGGBB</color>
```

```
android:backgrounnd = "@color/..."
```

### V1

How to add new views to your layout.

  - set id of a view: particular useful for findViewByID()

How to constrain the position of a view to another view.

```
app:layout_constraintBottom_toTopOf="@id/..."
```

  - **If a view is not constrained, it will move to (0, 0) at runtime**

```
app:layout_constraintVertical_bias
```
  
  - The "bias" constraints allows you to tweak the position of a view to be more on one side than the other when both sides are constrained in opposite directions.
  
chain: constraints link two or more objects to each other

### V2

*Enable auto import to import classes necessary for the Kotlin code*

How to find a view by its ID; how to show a toast message

```
// find the toast_button by its ID and set a click listener
view.findViewById<Button>(R.id.toast_button).setOnClickListener {
   // create a Toast with some text, to appear for a short time
   val myToast = Toast.makeText(context, getString(R.string.toast_text), Toast.LENGTH_SHORT)
   // show the Toast
   myToast.show()
}
```

How to add click listeners for a view.

  -To implement more complex functions, especially those that involve other views, it is a good practice to define functions.
  
 ```
  private fun countMe(view: View) {

}
```
```
Psuedocode to change a textView:

Input: a string to be displayed in textView

Output: the modified textView that shows the input string

1. Get the textView by getViewById

2. Read the value of the textView and convert it to the suitable data type

3. Modify the value by suitable logic 

4. Set the value of the textView by accessing its text field

```

Example function of incrementing the number in textView by 1:

```
private fun countMe(view:View) {
        // 1. Find the textView by findViewById
        val countTextView = view.findViewById<TextView>(R.id.number_text)
        // 2. Read the value from textView and convert it into int
        val countString = countTextView.text.toString()
        var count = countString.toInt()
        // 3. Modify the value with suitable logic
        count++
        // 4. Put the value back in string and into the textView
        countTextView.text = count.toString()
    }
 ```

How to set and get property values of a view from your code.

### V3

How to pass information to a second fragment.

### V4

### V5

### V6

### V7

### V7+
