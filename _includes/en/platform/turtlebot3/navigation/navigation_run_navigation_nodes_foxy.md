
1. If the `Bringup` is not running on the TurtleBot3 SBC, launch the Bringup. **Skip this step if you have launched bringup previously**.  
  - Open a new terminal from Remote PC with `Ctrl` + `Alt` + `T` and connect to Raspberry Pi with its IP address.
The default password is **ubuntu**.  
**[Remote PC]**    
  ```bash
$ ssh ubuntu@{IP_ADDRESS_OF_RASPBERRY_PI}
$ export TURTLEBOT3_MODEL=${TB3_MODEL}
$ ros2 launch turtlebot3_bringup robot.launch.py
  ```

2. Open a new terminal from Remote PC with `Ctrl` + `Alt` + `T` and launch the Navigation node. ROS 2 uses [Navigation2][nav2].
  Please use the proper keyword among `burger`, `waffle`, `waffle_pi` for the `TURTLEBOT3_MODEL` parameter.  
**[Remote PC]**  
  ```bash
$ export TURTLEBOT3_MODEL=burger
$ ros2 launch turtlebot3_navigation2 navigation2.launch.py map:=$HOME/map.yaml
  ```

<details>
<summary>
![](/assets/images/icon_unfold.png) **How to save the TURTLEBOT3_MODEL parameter?**
</summary>
The `$ export TURTLEBOT3_MODEL=${TB3_MODEL}` command can be omitted if the **TURTLEBOT3_MODEL** parameter is predefined in the `.bashrc` file.  
The `.bashrc` file is automatically loaded when a terminal window is created.  

- Example of defining `TurtlBot3 Burger` as a default model.  
**[Remote PC]**  
```bash
$ echo 'export TURTLEBOT3_MODEL=burger' >> ~/.bashrc
$ source ~/.bashrc
```

- Example of defining `TurtlBot3 Waffle Pi` as a default model.  
**[Remote PC]**  
```bash
$ echo 'export TURTLEBOT3_MODEL=waffle_pi' >> ~/.bashrc
$ source ~/.bashrc
```
</details>