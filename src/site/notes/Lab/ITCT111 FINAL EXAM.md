---
{"dg-publish":true,"permalink":"/lab/itct-111-final-exam/"}
---

# Smiley
![Pasted image 20240328033146.png](/img/user/Utilities/Attachments/Pasted%20image%2020240328033146.png)
## Class
```java
class Smiley{
  int x;
  int y;
  int size;
  public Smiley(int x, int y, int size)
  {
    this.x = x;
    this.y = y;
    this.size = size;
  }

  void render()
  {
    ellipseMode(CENTER);
    ellipse(x, y, size, size);
    int offsetX = size/2;
    int eyeSize = size/3;
    ellipse(x - offsetX, y, eyeSize, eyeSize);
    ellipse(x + offsetX, y, eyeSize, eyeSize);
  }

} // End of Class
```

## STARTER
```java
Smiley s;


void setup()
{
  size(400,400);
  s = new Smiley(width/2, height/2, 64);
}


void draw()
{
  s.render();
}
```

# Questions
## Q1
![Pasted image 20240328033207.png](/img/user/Utilities/Attachments/Pasted%20image%2020240328033207.png)
```java
Smiley s1;
Smiley **s2**;
Smiley s3;
Smiley **s4**;
Smiley **s5**;


void setup()
{
  size(400,400);
  s1 = new Smiley(width/2, 64, 64);
  s2 = new Smiley(width/2, **64*2**, 64);
  s3 = new Smiley(width/2, **64*3**, 64);
  s4 = new Smiley(width/2, **64*4**, 64);
  s5 = new Smiley(width/2, **64*5**, 64);
}


void draw()
{
  s1.render();
  **s2.render();**
  **s3.render();**
  **s4.render();**
  **s5.render();**
}
```

## Q2
![Pasted image 20240328033521.png](/img/user/Utilities/Attachments/Pasted%20image%2020240328033521.png)
```java
void setup()
{
  size(400,400);
  Smiley reusableSmiley = new Smiley(0, 0, 64);
  for(int i = 0; i < 4; i++)
  {
    reusableSmiley.x = width/2;
    reusableSmiley.y = 64 + i*64;
    reusableSmiley.render();
  }
}
```

## Q3
![Pasted image 20240328050727.png](/img/user/Utilities/Attachments/Pasted%20image%2020240328050727.png)
```java
void setup()
{
  size(400, 400);
  Smiley reusableSmiley = new Smiley(0, 0, 64);
  for (int i = 0; i < 5; i ++)
  {
    reusableSmiley.x = width/2;
    if ( i > 0 && i % 2 == 0) // Left
    {
      reusableSmiley.x = width/2 - 64;
    } else if ( i > 0 && i % 2 == 1) // Right
    {
      reusableSmiley.x = width/2 + 64;
    }
    reusableSmiley.y = 64 + i*64;
    reusableSmiley.render();
  }
}
```

## Q4
![Pasted image 20240328050923.png](/img/user/Utilities/Attachments/Pasted%20image%2020240328050923.png)
```java
int startX = 0;
int startY = 0;
int startRow = 5; // Always Odd Number that more than or equal to 3
int size = 64;

void setup()
{
  size(640, 640);

  Smiley reusableSmiley = new Smiley(0, 0, size);

  for (int j = 0; j < startRow; j++)
  {
    int col = startRow-j;
    for (int i = 0; i < col; i ++)
    {
      startX = size/2;
      reusableSmiley.x = startX + size*i;
      reusableSmiley.y = 32 + size*j;
      reusableSmiley.render();
    }
  }
}
```

## Q5
![Pasted image 20240328050930.png](/img/user/Utilities/Attachments/Pasted%20image%2020240328050930.png)
```java
int startX = 0;
int startY = 0;
int startRow = 5; // Always Odd Number that more than or equal to 3
int size = 64;


void setup()
{
  size(640, 640);

  Smiley reusableSmiley = new Smiley(0, 0, size);

  for (int j = 0; j < startRow; j++)
  {
    int col = startRow-j;
      for (int i = 0; i < col; i ++)
    {
      startX = size/2;
        reusableSmiley.x = startX + size*i;
        reusableSmiley.y = 32 + size*j;
        reusableSmiley.render();
    }
  }
  // Your Code Here for Q5
  for (int j = 0; j < startRow; j++)
  {
    int col = startRow-j;
      for (int i = 0; i < col; i ++)
    {
      startX = size/2;
        reusableSmiley.x = startX + size*i;
        reusableSmiley.y = 32 + size*j + (height/2);
        reusableSmiley.render();
    }
  }
}
```

## Q6
![Pasted image 20240328050937.png](/img/user/Utilities/Attachments/Pasted%20image%2020240328050937.png)
```java
int startX = 0;
int startY = 0;
int startRow = 5; // Always Odd Number that more than or equal to 3
int size = 64;


void setup()
{
  size(640, 640);

  Smiley reusableSmiley = new Smiley(0, 0, size);

  for (int j = 0; j < startRow; j++)
  {
    int col = startRow-j;
    for (int i = 0; i < col; i ++)
    {
      startX = size/2;
      reusableSmiley.x = startX + size*i;
      reusableSmiley.y = 32 + size*j;
      reusableSmiley.render();
    }
  }
  // Your Code Here for Q6
  for (int j = 0; j < startRow; j++)
  {
    int col = j+1;
    for (int i = 0; i < col; i ++)
    {
      startX = size/2;
      reusableSmiley.x = startX + size*i;
      reusableSmiley.y = 32 + size*j + height/2;
      reusableSmiley.render();
    }
  }
}
```

## Q7
![Pasted image 20240328051010.png](/img/user/Utilities/Attachments/Pasted%20image%2020240328051010.png)
```java
int N = 5;
int row = (N+1)/2;
int size = 64;

void setup() {
  size(640,640);
  rectMode(CENTER);
  
  for (int j = 0; j<row; j++) {
    int elements = N-j;
    for (int i = 0; i<elements; i++) {
      if (j%2==0){
        ellipse(32+i*size,32+j*size,size,size);
      }
      else if (j%2!=0){
        rect(32+i*size,32+j*size,size,size);
      }
    }
  }
}
```