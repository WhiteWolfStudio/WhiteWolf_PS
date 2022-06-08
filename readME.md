More comfortable library for using PlayStation Dualshock 4

For using please install Unity Input System:

* Windows
  * Package Manager
    * Select Unity Registry
      * Install "Input System"


# How use files and commands

* [Main File](#WW_PC.cs)
* [For Left Stick](#LeftStick.cs)
* [For Right Stick](#RightStick.cs)
* [For Buttons](#Buttons.cs)
* [For Arrows](#Arrows.cs)
* [For L1/L2/L3](#L.cs)
* [For R1/R2/R3](#R.cs)

# WW_PC.cs - Main File for work

``` csharp
bool debug  /* On true variable concole will show pressed keys */
bool work   /* All will be work if controller connected */

void DebugMode()    /* Use in script for switch debug variable */
string DebugInfo()  /* Need for Editor UI */
string WorkInfo()   /* Need for Editor UI */
string CountInfo()  /* Need for Editor UI */

/* For controll controller connection */
/* When controller disconected, you will have message about this */
void TestConnect() or Connect()
```

<hr />

# LeftStick.cs

``` csharp
using WhiteWolf.PS.Left

public class Example : MonoBehaviour {

    private void Start(){

        // bool
        // Simple info about slider
        LeftStick.Up();
        LeftStick.Left();
        LeftStick.Down();
        LeftStick.Right();

        // float
        // More information ( 0.0f, 1.0f )
        LeftStick.Value.Up();
        LeftStick.Value.Left(); 
        LeftStick.Value.Down(); 
        LeftStick.Value.Right(); 

        // float
        // Detail information about stick position X or Y
        LeftStick.XY.X();
        LeftStick.XY.Y();

    }

}
```

<hr />

# RightStick.cs

``` csharp
using WhiteWolf.PS.Right

public class Example : MonoBehaviour {

    private void Start(){

        // bool
        // Simple info about slider
        RightStick.Up();
        RightStick.Left();
        RightStick.Down();
        RightStick.Right();

        // float
        // More information ( 0.0f, 1.0f )
        RightStick.Value.Up();
        RightStick.Value.Left(); 
        RightStick.Value.Down(); 
        RightStick.Value.Right(); 

        // float
        // Detail information about stick position X or Y
        RightStick.XY.X();
        RightStick.XY.Y();

    }

}
```

<hr />

# Buttons.cs

``` csharp
using WhiteWolf.PS.Buttons

public class Example : MonoBehaviour {

    private void Start(){

        // bool
        // In if ( someButton() ){ doSomething(); }
        // ONLY FOR ONE CLICK!!!
        Buttons.Cross(); // ✖
        Buttons.Square(); // ■
        Buttons.Triagle(); // ▲
        Buttons.Circle(); // ●

        // bool
        // In if ( someButton() ){ doSomething(); }
        // NOT for one click!!!
        Buttons.Press.Cross(); // ✖
        Buttons.Press.Square(); // ■
        Buttons.Press.Triagle(); // ▲
        Buttons.Press.Circle(); // ●

    }

}
```

<hr />

# Arrows.cs

``` csharp
using WhiteWolf.PS.Arrows

public class Example : MonoBehaviour {

    private void Start(){

        // bool
        // In if ( someButton() ){ doSomething(); }
        // ONLY FOR ONE CLICK!!!
        Arrows.Up(); // ↑
        Arrows.Left(); // ←
        Arrows.Down(); // ↓
        Arrows.Right(); // →

        // bool
        // In if ( someButton() ){ doSomething(); }
        // NOT for one click!!!
        Arrows.Press.Up(); // ↑
        Arrows.Press.Left(); // ←
        Arrows.Press.Down(); // ↓
        Arrows.Press.Right(); // →

    }

}
```

<hr />

# L.cs

``` csharp
using WhiteWolf.PS.L

public class Example : MonoBehaviour {

    private void Start(){

        // bool
        // In if ( someButton() ){ doSomething(); }
        // ONLY FOR ONE CLICK!!!
        L.L1(); // Click on L1
        L.L2(); // Click on L2
        L.L3(); // Click on L3

        // float
        // In if ( someButton() ){ doSomething(); }
        // For get value of click ( 0.0f, 1.0f )
        // Only L2
      	L.Value.L2();

    }

}
```

<hr />

# R.cs

``` csharp
using WhiteWolf.PS.R

public class Example : MonoBehaviour {

    private void Start(){

        // bool
        // In if ( someButton() ){ doSomething(); }
        // ONLY FOR ONE CLICK!!!
        R.L1(); // Click on R1
        R.L2(); // Click on R2
        R.L3(); // Click on R3

        // float
        // In if ( someButton() ){ doSomething(); }
        // For get value of click ( 0.0f, 1.0f )
        // Only R2
      	L.Value.R2();

    }

}
```

<hr />

``` csharp
/*
 __   __   __         ______     _____     __    __     ______     ______     __  __     ______    
/\ \ /  / /\ \       /\  __ \   /\  __-.  /\ "-./  \   /\  __ \   /\  ___\   /\ \/ /    /\  __ \   
\ \ \' /  \ \ \____  \ \  __ \  \ \ \/\ \ \ \ \-./\ \  \ \  __ \  \ \___  \  \ \  _"-.  \ \  __ \  
 \ \__/    \ \_____\  \ \_\ \_\  \ \____-  \ \_\ \ \_\  \ \_\ \_\  \/\_____\  \ \_\ \_\  \ \_\ \_\ 
  \/_/      \/_____/   \/_/\/_/   \/____/   \/_/  \/_/   \/_/\/_/   \/_____/   \/_/\/_/   \/_/\/_/ 
                                                                                                   
*/
```
