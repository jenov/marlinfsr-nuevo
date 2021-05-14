### **TIPS-SLICER** 
  
  In your **Start_GCode** on your Slicer.
  - M420 S1 enable bed leveling but in my firmware G28 activate the last mesh used or the default one (0)
  - M420 Lx or G29 Lx (Load mesh_x correction). 
    If you are using PrusaSlicer you can add a line "*G29 Lx; load mesh PLA*" in the **Filament** starting GCode instead of the G29 Lx in the printer start GCode.

  And on my **EndGCode** I remove G28 and I substitute with this type of code:

        {if layer_z <max_print_height} G1 Z {min (layer_z + 100, max_print_height)} {endif} F4000

  This works fine in [PrusaSlicer](https://help.prusa3d.com/en/article/macros_1775) and goes 100cm above the finished object. It's up to you to adapt it for your favorite Slicer or to improve mine.

  ### **You will find some Slicer profiles in the "Slicers" [directory](../Slicers).** 

![Final_Print](../../docs/images/Final.png)
![Presentation](../../docs/images/Final2.jpg)

![Tests](../../docs/images/Tests.png)
![MotorMounts](../../docs/images/BottomPulley.png)
***