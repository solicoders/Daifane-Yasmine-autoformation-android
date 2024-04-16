---
layout: default
chapitre: Configurer android studio
presentation: Configurer android studio
order: 4
---

# Créer une mise en page de base
### Question 
- Créer une mise en page de baseDonnez les définitions des termes suivants :
    - sp
    - dp
  
### Solution 
  - Scalable pixels
  - The scalable pixels (SP) is a unit of measure for the font size. 
  - UI elements in Android apps use two different units of measurement: 
  
    - density-independent pixels (DP), which you use later for the layout, and scalable pixels (SP).
  -  By default, the SP unit is the same size as the DP unit, but it resizes based on the user's preferred text size under phone settings. 

## Using ROw and Column

 ```bash
  Row {
        Text(
            text = message,
            color = Color.Green,
            fontSize = 30.sp,
            lineHeight = 116.sp,
            textAlign = TextAlign.Center
        )
        Text(
            text = from,
            fontSize = 36.sp,

        )
    }
```

```bash
 Column (  verticalArrangement = Arrangement.Center,
        modifier = modifier) {

            Text(
                text = message,
                 modifier = Modifier.background(color = Color.Green),
                color = Color.Green,
                fontSize = 100.sp,
                lineHeight = 116.sp,
                textAlign = TextAlign.Center
            )
            Text(
                text = from,
                fontSize = 36.sp,
                modifier = Modifier
                    .padding(16.dp)
                    .align(alignment = Alignment.End)
                )

    }
```

## Add an image 

```bash
@Composable
fun GreetingImage(message: String, from: String, modifier: Modifier = Modifier) {
    val image = painterResource(R.drawable.androidparty)
    Image(
        painter = image ,
        contentDescription = null ,
        contentScale = ContentScale.crop, 
             alpha = 0.5F , 


 )
 }
@Preview(showBackground = true)
@Composable
fun BirthdayCardPreview() {
    HappyBirthdayTheme {
        GreetingImage(
            message = "Happy Birthday Sam!",
            from = "From Emma"
        )
    }
}

```

## Using compsal Box to add text on top of image

```bash
@Composable
fun GreetingImage(message: String, from: String, modifier: Modifier = Modifier) {
    val image = painterResource(R.drawable.androidparty)

   Box(modifier){
       Image(
           painter = image ,
           contentDescription = null

       )

       GreetingText(
           message = message,
           from = from,
           modifier = Modifier
               .fillMaxSize()
               .padding(8.dp)
       )
   }
}
@Preview(showBackground = true)
@Composable
fun BirthdayCardPreview() {
    HappyBirthdayTheme {
        GreetingImage(
            message = "Happy Birthday Sam!",
            from = "From Emma"
        )
    }
 }

```