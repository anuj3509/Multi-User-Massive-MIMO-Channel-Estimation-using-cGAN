# Multi-User Massive MIMO Channel Estimation using cGAN

# 1. Steps to Generate Data
1. Download "I1_2p4.zip" from this link: https://drive.google.com/drive/folders/1rbIHfK__JUn5e52y5GWI7p-0cL5OSZUO?usp=sharing.
2. In the main repository, navigate to Data_Generation_matlab.
3. Next, extract the "I1_2P4" .zip file and put it in the folder "Data_Generation_matlab/RayTracing Scenarios".
4. Run the matlab function **"Data_Generation_matlab/GenerateData_Main.m"** to generate channel data and quantized signal data.
5. Run the GenerateData_MainLoop.m file on your local machine.
6. This will generate dataset at varying number of antennas (in this case, M = 64, 128, 192, 256, 512) each iterating over SNR values of [-10, -5, 0, 5, 10, 15, 20, 25, 30, 35, 40].
7. I have created a sample datset for 64 base station anennas over SNR values = [-5, 0, 5, 10, 15, 20]. But the code has provision of generating more. Datasets other than these very significantly large to push. You can view it here: **"Data_Generation_matlab/Gan_Data/Gan_10_dBIndoor2p4_64ant_32users_8pilot.mat"**, which inculdes the channel data and quantized signal data.

# 2. Steps for Code Execution
1. Run the file project_final.ipynb after generating data as described in Section 1.
2. Make sure to change the variable **path** wherever required according to your google drive path where you stored the files on mounting.
3. Feel free to tweak any parameters for increased accuracy.
4. After each epoch you will see that the code will generate images with Input Y, Targeted and Predicted H along with an error value on the plot.
