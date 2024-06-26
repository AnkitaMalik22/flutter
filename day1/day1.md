## Flutter: Most Used Widgets and Hierarchy

This document outlines some of the most commonly used widgets in Flutter and their hierarchical relationships for building user interfaces.

**Understanding Widget Hierarchy:**

In Flutter, everything is a widget. Widgets are the building blocks that you assemble to create user interfaces. Widgets can be combined to create more complex widgets, forming a hierarchy.

**Common Widgets:**

1. **Container:** The fundamental widget for laying out other widgets. It provides padding, margins, borders, and background decoration for its child widgets.

2. **Row & Column:** These widgets arrange child widgets horizontally (Row) or vertically (Column). They are essential for structuring layouts.

3. **Text:** Used to display text content. It offers various properties for styling the text (font size, color, etc.).

4. **Image:** Used to display images from assets or network URLs.

5. **ElevatedButton & IconButton:** Buttons for user interaction. ElevatedButton has a raised appearance, while IconButton is typically used for smaller, icon-based buttons.

6. **Padding & Margin:** Widgets to add space around child widgets. Padding adds space within the container's borders, while Margin adds space outside the borders.

7. **Stack & Overlay:** Used for layering widgets on top of each other. Stack positions widgets absolutely within its bounds, while Overlay allows more flexible positioning throughout the screen.

8. **ListView & GridView:** Used to display scrollable lists of items. ListView arranges items linearly, while GridView arranges them in a grid format.

9. **AppBar:** Represents the top app bar containing the app title, navigation icons, and potentially actions.

10. **Scaffold:** The most common layout structure in Flutter apps. It provides a basic framework with AppBar, body (usually a Container), and optional elements like a floating action button and bottom navigation bar.

**Hierarchy Example:**

Here's a simplified example of a widget hierarchy for a product card:

```
Scaffold (
  appBar: AppBar(
    title: Text('My Shop'),
  ),
  body: Container(
    padding: EdgeInsets.all(16.0), // Add padding
    child: Row( // Arrange widgets horizontally
      children: [
        Image.network('https://example.com/product_image.jpg', width: 100.0),
        Column( // Arrange information vertically
          crossAxisAlignment: CrossAxisAlignment.start, // Align text to the left
          children: [
            Text('Product Title'),
            Text('Price: \$10.00'),
            ElevatedButton(onPressed: () {}, child: Text('Buy Now')),
          ],
        ),
      ],
    ),
  ),
);
```

