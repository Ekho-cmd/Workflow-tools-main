# Workflow-tools-main
Google Sheet used as a standard format for maintenance, fuel usage, job details, and job calculations. 

Unit:
  Physical location of the unit on the site.
  
Pump:
  Unit specific numeric identifier.
  
Dual Fuel / Diesel Only:
  Denotes whether the unit is capable of using Dual Fuel (natural gas & diesel) or diesel only for fuel.
  Additional selections are as follows:
    Offline for Maintenance - The unit will not be used during the job due to maintenance issues.
    Offline for Gas+ - The unit will not be used during the job in order to increase natural gas usage on the remaining online units.

Using Gas Yes/No:
  Selection to indicate whether the online dual fuel units are actually using gas during the job, or not.
  
% (Percentage):
  Input the percentage each unit is substituting diesel fuel with natural gas during the job.
  
Issues:
  Record any issues identified with the unit, specifically in relation to the dual fuel system.
  
Comments:
  Record any comments related to the equipment in general for current job.
  
Diesel Skid Calculator:
  Calculator that takes diesel fuel skid levels in inches and converts them to gallons. Used to record diesel fuel consumption for the previous job.
         
Date:
  Input for the date of the beginning of the job.
  
Well Name: 
  Input the well identifier.
  
Stage:
  Input the stage (job) number.
  
Gas Beginning:
  Measurement reading from the natural gas skid totalizer before beginning the a job.
  
Stage Start:
  Input the time at the start of the stage (job).
  
Gas Pressure:
  Measurement reading from the pressure transducer on the natural gas skid manifold.
  
Gas Temperature:
  Measurement reading from the thermometer probe on the natural gas skid manifold.
  
Stage End:
  Input the time at the end of the stage (job).
  
Minutes @ Rate:
  Input the total length of time the job has been ran at designed rate, in minutes.
  
Avg Rate:
  Input the average rate (bpm) the job was pumped from the time proppant was introduced.
  
Avg Pressure:
  Input the average pressure (psi) the job was pumped fro the time proppant was introduced.
  
Gas Ending:
  Measurement reading from the natural gas skid totalizer taken after the a job.
  
Diesel Used:
  Combined total of diesel fuel in gallons, used for the job. Taken from the Diesel Skid Calculator.
  
Gas Used:
  Total natural gas used for the job in Mcf. Result from the difference of the "Gas Beginning" and "Gas Ending".
  
Gas Pumps:
  Total number of dual fuel pumps using gas for the stage. Result from the sum of dual fuel pumps in the "Dual Fuel / Diesel Only" column && the "Using Gas Y/N" column.
  
Online Pumps:
  Total number of dual fuel and diesel only pumps used for the stage. Result from the sum of dual fuel pumps in the "Dual Fuel / Diesel Only" column && the "Using Gas Y/N"     column, && the sum of the diesel only pumps.
  
Stage Length:
  Total length of the stage in hours and minutes. Result from the difference of "Stage Start" and "Stage End".
  
Pad Avg Mcf/P:
  Average natural gas usage per pump. Taken fron the running average of Mcf used per stage and the running average of dual fuel pumps per stage on the "Log" sheet.
  
Pad Avg Mcf:
  Running average natural gas usage over the life of the pad.
  
Fleet Sub %:
  Running percentage of diesel fuel substitution by natural gas over the life of the pad. Calculated from the sustitution column on the "Log" sheet.
  
Pad Avg HHP/P:
  Running average of hydraulic horsepower per pump over the life of the pad. Calculated from the hydraulic horsepower and total pumps online columns on the "Log" sheet.
  
Gallons/Stage Count (Chart):
  Chart representing the changes in gallons of diesel fuel used by stage count.
  
MCF/Stage Count (Chart):
  Chart representing the changes in natural gas usage (Mcf) by stage count.
  
Green Arrow Button:
  When clicked, initiates the execution of the "Main Function".
  
<img width="940" alt="Equipment Sheet" src="https://user-images.githubusercontent.com/84663264/119502518-0256e700-bd38-11eb-9efa-59ac4edf4fcf.png">

<img width="894" alt="Tracker Sheet" src="https://user-images.githubusercontent.com/84663264/119368565-273c5300-bc81-11eb-9fe4-615c69898db7.png">

<img width="705" alt="Proppant Sheet" src="https://user-images.githubusercontent.com/84663264/119479772-fca0d780-bd1e-11eb-9913-66539cf62d03.png">

<img width="585" alt="Log Sheet" src="https://user-images.githubusercontent.com/84663264/119368578-2d323400-bc81-11eb-9881-0004fcc0debf.png">



