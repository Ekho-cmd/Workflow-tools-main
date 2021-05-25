# Workflow-tools-main
Google Sheet used as a standard format for maintenance, fuel usage, job details, and uses Google Apps Script and cell residing formulas to perform calculations.

*Equipment Sheet:
  Used to input equipment and job details per stage. Input is then submitted to the "Log" sheet for record keeping and life of pad calculations.

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

*Fluid End Maintenance Tracker
  Tracker sheet is used to provide a visual indicator for equipment maintenance time intervals. When a unit leaves the site, the Remove function is used transfer the unit       information to a running log below the tracker as a quick reference for when the unit returns.

Check units to be removed from tracker:
  When a unit needs to leave the site, the corresponding checkbox can be selected and the "Remove" button clicked. This will initiate the execution of the "TrackerMain"         function and copy the unit information to the log below the tracker. Once transfered, the unit information will be cleared so the new unit information can be entered.
  
Position:
  Denotes the physical location of the unit on the site.
  
Unit Number:
  Input for the unit number of the unit in this location.
  
Usage:
  Selection for the type of fluid the unit will use during the job. "Clean" is described as water that does not have proppant or acid in it; "Dirty" is described as water       that has proppant mixed with it as a slurry, and does not use acid; "Acid" is described as a clean or dirty pump that will use either acid or acid mixed with water.
  
Select Seat Type:
  Selection for the type of valve seat installed in the fluid end. "Conv." is described as a stainless steel seat; "Carbide" is described as a high-carbon steel seat.
  
Current Pump Strokes:
  Input is entered as the current totalized strokes of the power-end pony rods. In the context of this sheet it is only used as a measurment of usage for calculating maintenance intervals.
  
Last Valve Change:
  Input is entered as the stroke count at the last time the fluid end valves were replaced or inspected.
  
Last Seat Change:
  Input is entered as the stroke count at the last time the fluid end seats were replaced or inspected.
    
Last Packing Change:
  Input is entered as the stroke count at the last time the fluid end packings were replaced or inspected.
  
Last Check Valve Inspection:
  Input is entered as the stroke count at the last time the unit check valve was inspected, repaired, or replaced.
  
Valves:
  Result of calculating the difference between the current stroke count and the previous valve change, divided by the variable valve setpoint. Shown as a percentage.
  
Seats:
  Result of calculating the difference between the current stroke count and the previous seat change, divided by the variable seat setpoint. Shown as a percentage.
  
Packing:
  Result of calculating the difference between the current stroke count and the previous packing change, divided by the variable packing setpoint. Shown as a percentage.
  
Check Valve:
  Result of calculating the difference between the current stroke count and the previous 'valve' change, divided by the variable check valve setpoint. Shown as a percentage.
  
Comments:
  Cell to input any issues relating to the unit.
  
Stroke Interval Setpoints:
  Inputs to declare the stroke interval used in calculations to output the various component usage as a percent.
  
 Maintenance Tracker Log:
  Area where the output of the "TrackerMain" function resides when the "Remove" button has been clicked. This is used as a quick reference to identify the details of a unit the last time it left the site.

<img width="891" alt="Tracker Sheet" src="https://user-images.githubusercontent.com/84663264/119516872-1ce38d00-bd45-11eb-9e18-0f6f16662def.png">

*Proppant Sheet:
  Google sheet used to keep track of proppant volumes in the onsite bins/silos. Calculates negative volumes to transport loads needed to start a stage.
  
Proppant Scheduled:
  (Row 1) Input the volume of ech proppant type scheduled for the job as dictated by the job design.
  
Proppant Storage (A):
  (Row 2) Select the scheduled proppant type.
  
Proppant Storage (B):
  (A3:B10) Indicates the bin/silo number and what proppant types stored in the respective container.
  
Proppant Storage (C):
  (C3:G10) Input to enter proppant volumes respective to the corrosponding container.
  
Comments: 
  Input comments or equipment issues relavent to the corrosponding container.
  
Proppant Totals:
  Sum total of proppant type on site.
  
Available Stages:
  Result of calculation using the proppant total divided by the proppant scheduled.
  
Go/No-Go:
  Visual and text indicator of whether the proppant total exceeds the proppant scheduled.
  
Loads Needed:
  Result of calculation using the difference of proppant scheduled and proppant totals to output the quantity of proppant loads needed to start a stage.
  
<img width="705" alt="Proppant Sheet" src="https://user-images.githubusercontent.com/84663264/119479772-fca0d780-bd1e-11eb-9913-66539cf62d03.png">

<img width="867" alt="Log Sheet" src="https://user-images.githubusercontent.com/84663264/119524196-6cc55280-bd4b-11eb-8866-ca493c7daf9f.png">




