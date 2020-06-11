# HATSim


Note:

This tool requires working internet connection and Matlab-Runtime (9.4) (https://www.mathworks.com/products/compiler/matlab-runtime.html) installed in the PC.



This tool simulates site-based synthetic ground-motions using DRD (aka ADK) simulation model (Razaeian et. al. 2012,  Dabaghi et. al. 2018b). The inputs for the Event parameters (such as F, Mw, Rrup) are obtained from USGS Unified Hazard Tool (2008) and the inputs for the Near-Fault parameters (such as Ztor, s or d, theta or phi) are randomized (Dabaghi et. al. 2018a) using Cybershake-UCERF2 database.



Instructions:

The primary inputs to this tool include: 'Edition', 'Longitude', 'Latitude', 'Vs30', 'Period of Structure', and 'Hazard Level'. These are used to obtain Deaggregation and Hazard Curves from USGS Unified Hazard Tool (2008). The data obtained from USGS is combined with the Cybershake-UCERF2 database to simulate the 'Required Number of GMs'. If the user selects the 'Yes' option, to 'Do you only want the GMs that match UHS at the specified Period of the Structure', then the simulated GMs will possess RotD50Sa between (UHS Sa) and (UHS Sa + Tolerance) using the algorithm proposed by Fayaz et. al. 2020.

USGS possess Hazard Curves and Deaggregation only for PGA and Periods = 0.2, 1.0, & 2.0 sec and Vs30 = 180, 259, 360, 537, 760 & 1150 m/s. Hence the Hazard Curves are generated only for these Periods and Deaggregation is conducted for the Period closest to the Period entered by the user.

'Seed No.' is an input for randomness and reproducibility, and must be a whole number. It will be concatenated to the input of 'Folder containing Results Output' for creating the folder for results. Hence, the results will be provided in a new folder named as per the inputs 'Folder containing Results Output-Seed No.'

This project was completed under the Caltrans Project Award No. 65A0647. For detailed information please read the report: 'Guidelines for Ground Motion Modeling for Performance-Based Earthquake Engineering of Ordinary Bridges' (Fayaz et. al. 2019).



Collaborators and Contributors:

Jawad Fayaz (UC-Irvine), Sarah Azar (AUB-Beirut), Yara Daoud (AUB-Beirut), Mayssa Dabaghi (AUB-Beirut), and Farzin Zareian (UC-Irvine).


    Primary citation for this tool :    
    Fayaz J., Azar S., Dabaghi M., and Zareian F. (2020). An Efficient Algorithm to Simulate Hazard-Targeted Site-Based Synthetic Ground Motions, Earthquake Spectra



References:

1) Fayaz J., Azar S., Dabaghi M., and Zareian F. (2020). An Efficient Algorithm to Simulate Hazard-Targeted Site-Based Synthetic Ground Motions, Earthquake Spectra

2) Dabaghi, M., Daoud, Y., and Der Kiureghian, A. (2018a). Simulation of near fault ground motions for randomized hypocenter and site locations, Proceedings of the 11th US National Conference on Earthquake Engineering, Los Angeles, CA.

3) Dabaghi M., and Der Kiureghian A. (2018b). Simulation of orthogonal horizontal components of near‐fault ground motion for specified earthquake source and site characteristics. Earthquake Engineering & Structural Dynamics; 47(6):1369-1393.

4) Rezaeian, S., and Der Kiureghian, A., (2012). Simulation of orthogonal horizontal ground motion components for specified earthquake and site characteristics. Earthquake Engineering & Structural Dynamics; 41(2), 335-353.
