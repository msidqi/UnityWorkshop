####################################################################################################
Create 2 variables:

                        // Rigidbody2D is a Component that controls physics(like Velocity, Gravity, Mass, etc..)
private Rigidbody2D rb; // Here, we created a Rigidbody2D-Type variable and we called it "rb")

private float speed; // (this is the variable that will controll how fast the character will move)

_________________________________________________________________________________________________
Result:


private Rigidbody2D rb;
private float speed;

void Start () {                        // Start function is called only once; that's when the game starts.


    speed = 10;                               // we initialized speed by 10
    rb = GetComponent<Rigidbody2D>();         // we initialized rb variable with the player's Rigidbody2D
}


####################################################################################################
Now let's move the Player:

void Update () {                       // Update function is called ~60 times every second(depending on the hardware).


    if (Input.GetKey(KeyCode.D))    
        rb.velocity = speed * Vector2.right;    // if the key pressed is "D" we change the velocity to = 10 * (1, 0). 

    else if (Input.GetKey(KeyCode.A))
        rb.velocity = speed * Vector2.left;     // else it is changed to = 10 * (-1, 0).
}
