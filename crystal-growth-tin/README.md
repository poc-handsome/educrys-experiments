
A systematic lab manual is provided in [manual](/crystal-growth-tin/manual) (TODO) while the sections below introduce a basic experiment.

## Preparing the hardware

- Switch on the EduCrys setup by connecting the power cable
- Login to the Raspberry Pi OS
- Check and adjust the clock on Raspberry Pi (important for data logging)
- Adjust the camera position and focus. This command in the Terminal could be used: ```libcamera-still -t 0```, terminated with Ctrl + C after the adjustment.
- Start the GUI
- Use GUI elements to check that all hardware components work:
  - All 3x motors start moving
  - All sensors show realistic values. Touch the temperature sensors by hand and observe temperature increase. Push slightly on the weight cell.
  - Camera and infrared images are shown. Put your hand in the front of the infrared sensor and observe the image.
  - LED lights up  
  - Heating starts if a 50 °C is temporarily set as target temperature. The red power light of the hotplate in the slit of the top wall should go on and off

## Preparing the experiment

- Prepare a 20x1 mm copper wire as a first artificial seed. Fix it in the seed holder
- Move the seed holder (bottom) 100 mm above the crucible, set the Z position in the GUI
- Tare the weight cell to zero

## Heating

- Set the cooling fan to 30%
- Start a recipe with a temperature ramp to 220 °C in 30 min, followed by a ramp to 237 °C in 15 min. Such ramps reduce the overshooting of the temperature control. The temperature should become stable approx. after 1 h after heating start.
- Remove the golden-color oxide from the surface with a stainless steel spoon once the tin melts. This needs to be repeated several times especially with fresh raw material. Oxidation increases rapidly with temperature, so overheating the tin above 250 °C should be avoided.

## Seed growth

- Immerse the artificial copper seed for about 3 mm into the melt at the center. The gamepad is useful for controlling the seed motion.
- Slightly touch the seed holder with the metal ruler, so that a good meniscus shape is formed at the seed
- Start pulling with about 5 mm/min. Increase the speed in steps by about 1.5x to 30...40 mm/min, until the crystal diameter decreases to 1...1.5 mm.
- The crystal may detach from the melt if the pull speed is increased too fast or if there was too much oxide on the surface
- Stop the growth before the seed holder comes too close to the weight cell. **Pulling may not stop automatically if the Z coordinate is not set correctly**.
- Cut the grown crystal in peaces of about 20 mm length. Straighten out these pieces by rolling them between the metal ruler and a hard flat surface.

## Crystal growth

- Fix a tin seed in the seed holder
- Immerse the seed into the melt as described above
- Start pulling with slow velocity of about 2...3 mm/min to obtain crystal diameter of 10...15 mm. Crystal diameter is also influenced by the melt temperature (and fan cooling). A virtual [simulation](https://github.com/nemocrys/crystal-game) for these physical effects is available and also installed on EduCrys. Further literature is also available on the project [website](https://poc-handsome.github.io/details/details.html)
- Once the desired crystal length is achieved, shortly increase the growth speed to 30...50 mm/min to detach the crystal from the melt. 

## Cooling

- Set the target temperature to 20 °C to switch off the hot plate. Increase the fan speed to 60%
- A complete cooldown may require more than an hour.
- Remove the seed and crystal from the seed holder once they are cold

## Analysis

- Measure crystal diameter at several positions
- Observe the growth ridges on the crystal surface, which indicate the crystalline structure. It is possible that a single crystal is obtained. 
- Analye the data in the experiment folder containing all image and log files 
- Create plots of process parameters such as melt temperature and pull speed over time


