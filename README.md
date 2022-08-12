# PlutoSDR_BLE_Stream_Capturing

Here is showing the method to capture the BLE data stream with the ADALAM-PLUTO.

Where the RF coverage of PlutoSDR is from 325 MHz to 3.8 GHz, apperantly it's sufficient for 2.4GHz bandwidth.

With the ADALAM-PLUTO, we can realize the data capturing through Matlab, Simulink, Gnu Radio and so forth.


1_MATLAB

     Prerequisite: Pluto environment setting, we can follow the instruction (Capturing_Matlab.pdf).



2_GNU_Radio

      Prerequeisites: we need to configure the gnuradio-companion and libiio-util in Ubuntu (or Windows, Mac).

      We can check the connection between Pluto device and PC with the command iio_info -s in terminal.  
        
      PlutoSDR as a receiver, then we need a transmitter, so the Beacon Simulator (Conf_Beacon_Simulator.jpg) in mobile phone or other devices which equipped the BLE protocol can be realized this part. 
        
      We tried to capture some BLE data streams with the file called Pluto.grc, and please notice the sample rate we should set as 13*e6, because the I/Q signals still at the situation of upsampling.
      


3_Jupyter_Notebook

      Whatever the mathods of Matlab or Gnu Radio we would utilize, the final step we need to verify the correctness of data streams, so here we would use Jupyter notebook which bases on the python core, and it can illustrate the results of captured signal step by step. 
      
      Within the file Signal_Analysis.ipynb, we can realize the functions about file reading, data analysis and file writing and so forth.
      
      
      
4_Result_Analysis

      The file Stream_captured.pdf shows the analysis of result, and the important thing is to recognize the BLE sequences from theory to the practice. We can reference the resource https://inst.eecs.berkeley.edu/~ee290c/sp18/lec/Lecture7A.pdf 


        
      
        
    

    

   
