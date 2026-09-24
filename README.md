# Ex06-Redirect the Scene

### Name - R SUDHIR KUMAR
### Register number - 212223230221

## Aim:
To Redirecting the scene in the unity engine.

## Algorithm:
Step 1:
To open the unity engine.

Step 2:
Create a new 3D project.

Step 3:
Create plane and name it as ground and create cube and name it as player.

Step 4:
Add WinText in Hierarchy.

Step 5:
Create a C# Script and name it as playercontroller and add the script to player.

Step 6:
Use the R button to change the level2

Step 7
Print the Output and end the program.

## Program:
### CUBE PLAYER:

```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class Coding : MonoBehaviour
{
    Rigidbody rb;
    public GameObject WinText;
    // Start is called before the first frame update
    void Start()
    {
        rb = GetComponent<Rigidbody>();

    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("Level2");
        }

    }
    private void OnTriggerEnter(Collider other)
    {
        if (other.gameObject.tag == "Cube")
        {
            Destroy(other.gameObject);
            WinText.SetActive(true);
        }
    }
}

```
## Output:

<img width="1917" height="1052" alt="Screenshot 2026-09-24 155050" src="https://github.com/user-attachments/assets/d1263b45-68ec-409d-8887-9adb5964b1a7" />

<img width="1917" height="1078" alt="Screenshot 2026-09-24 155120" src="https://github.com/user-attachments/assets/0f138f26-6c16-4856-aa89-314e71708ae0" />

## Result:

Thus, the execution of above C# coding is successfully redirecting the scene in the unity engine.
