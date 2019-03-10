############################################################################################
Create 2 variables:

                        // Rigidbody2D is a Component that controls physics(like Velocity, Gravity, Mass, etc..)
                        // Here, we created a Rigidbody2D-Type variable and we called it "rb"
     private Rigidbody2D rb; 

                        // this is the variable that will controll how fast the character will move

     private float speed; 

__________________________________________________________________________________________
Result:


private Rigidbody2D rb;

private float speed;


  // Start function is called only once; that's when the game starts.
void Start () {                      


    speed = 10;                               // we initialized speed by 10
    rb = GetComponent<Rigidbody2D>();         // we initialized rb variable with the player's Rigidbody2D
}


###########################################################################################
Now let's move the Player:

 // Update function is called ~60 times every second(depending on the hardware).
void Update () {                      


    if (Input.GetKey(KeyCode.D))    
        rb.velocity = speed * Vector2.right;    // if the key pressed is "D" we change the velocity to = 10 * (1, 0). 

    else if (Input.GetKey(KeyCode.A))
        rb.velocity = speed * Vector2.left;     // else it is changed to = 10 * (-1, 0).
}

__________________________________________________________________________________________
Result:

As you might have noticed, the player rotates when you try to move the him with "A" and "D" buttons.
To fix this, simply freeze the Rotation by clicking on "Player" and then click on "RigidBody2D->Contraints->Freeze Rotation Z"
