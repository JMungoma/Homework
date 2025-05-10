# Section 1
### - 1.1 Review the column that you are looking to change
SELECT Accel FROM evCars

### - 1.2 Selecting the correct string function
RTRIM(string, character)

### - 1.3 Visualizing the changes before making them 
SELECT Accel, RTRIM(Accel, '  sec') 
FROM evCars

### - 1.4 UPDATE the records 
UPDATE evCars 
SET Accel = RTRIM(Accel, ' sec')

### - 1.5 Check your work
SELECT Accel FROM evCars;

### - 1.6 Rename the column
ALTER TABLE evCars
 RENAME Accel TO AccelSec;




# Section 2

### - 2.1 Review the column that you are looking to change 
SELECT TopSpeed FROM evCars;
### 2.2 Selecting the correct String Function
RTRIM(TopSpeed, '  kmh/h') 

### - 2.3 Visualizing the Changes before making them 
SELECT TopSpeed, RTRIM(TopSpeed, '  kmh/h') 
FROM evCars;

### - 2.4 UPDATE the records
UPDATE evCars
SET TopSpeed = RTRIM(TopSpeed, ' kmh/h');

### - 2.5 Check your work 
SELECT TopSpeed FROM evCars;

### - 2.6 Convert the units to MPH
SELECT TopSpeed, ROUND(TopSpeed * 0.621371, 1)
FROM evCars;

UPDATE evCars 
SET TopSpeed = TopSpeed * 0.621371;

### - 2.7 Rename the column
ALTER TABLE evCars
RENAME TopSpeed TO TopSpeedMPH;

### - 2.8  Select All of the records to get a look at the whole table with your recent changes. 
SELECT * 
FROM evCars


# Section 3 

### - 3.1 Review the column that you are looking to change 
SELECT Range FROM evCars;

### - 3.2 Selecting the correct String Function
RTRIM(Range, ' km')

### - 3.3 Visualizing the Changes before making them 
SELECT Range, RTRIM(Range, ' km') 
FROM evCars;

### - 3.4 UPDATE the records
UPDATE evCars
SET Range = RTRIM(Range, ' km')

### - 3.5 Check your work 
SELECT Range FROM evCars;

### - 3.6 Convert the units to MPH
SELECT Range, ROUND(Range * 0.621371, 1)
FROM evCars;

UPDATE evCars
SET Range = Range * 0.621371;

### - 3.7 Rename the column
ALTER TABLE evCars
RENAME Range TO RangeMiles;

### - 3.8  Select All of the records to get a look at the whole table with your recent changes. 
SELECT * from evCars;


# SECTION 4
### - 4.1 Write a select statement to review both of the columns that you are looking to change 
SELECT Efficiency FROM evCars;

### - 4.2 Selecting the correct String Function that we need to remove for each column.
RTRIM(Efficiency, ' Wh/km')
RTRIM(FastCharge, ' km/h')

### - 4.3 Visualizing the Changes before making them 
SELECT 
Efficiency, RTRIM(Efficiency, ' Wh/km'),
FastCharge, RTRIM(FastCharge, ' km/h')
FROM evCars;


### - 4.4 UPDATE the records
UPDATE evCars
SET 
Efficiency = RTRIM(Efficiency, ' Wh/km'),
FastCharge = RTRIM(FastCharge, ' km/h')

FastCharge = FastCharge * 0.621371;

### - 4.5 Check your work 
SELECT 
Efficiency,
FastCharge
FROM evCars;

### - 4.6 Convert the `FastCharge` units to MPH
SELECT 
FastCharge, ROUND(FastCharge * 0.621371, 1)
FROM evCars;

UPDATE evCars
SET FastCharge = ROUND (FastCharge * 0.621371, 1);

# Bonus: Rounding  FastCharge to 1 decimal place.
SELECT FastCharge, ROUND(FastCharge, 1)
FROM evCars;

### - 4.7 Rename the column
ALTER TABLE evCars
RENAME FastCharge TO OneHourFastChargeMiles;

ALTER TABLE evCars
RENAME Efficiency TO EfficiencyWHperKM;

## 4.8 Select All of the records to get a look at the whole table with your recent changes. 
SELECT * FROM evCars;

# SECTION 5 

### - 5.1 Working with `RapidCharge`
SELECT RapidCharge, COUNT(*)
FROM evCars
GROUP BY RapidCharge;

### - 5.2 Making data cleaning choices 
SELECT RapidCharge,
	CASE WHEN RapidCharge LIKE '%not possible' THEN 1
	ELSE 0
	END
FROM evCars;

### - 5.2 Writing the update Statements  
I need guidance how to complete the code. This is what I came up with:

UPDATE evCars
SET RapidCharge = "RapidCharging"
	CASE WHEN RapidCharge LIKE '%not possible' THEN 1
	ELSE 0
	END

### - 5.3 Please fill in the blank on your .md answer sheet
if the car's `RapidCharge` value equals 'Rapid charging possible' then I want you to change the value to 'Yes' 
- If the `RapidCharge` value equals 'Rapid charging not possible' then I want you to change the value to 'No'. 


# SECTION 6

### -6.1 Visualize the `Powertrain` records
SELECT PowerTrain, COUNT(*)
FROM evCars
GROUP BY PowerTrain;

### - 6.2 Please fill in the blank on your .md answer sheet
- look at the three DISTINCT values from the query you wrote in 6.1 and fill in the blanks.
- If the PowerTrain equals 'All Wheel Drive' then I want you to change the value to 'AWD'
- If the PowerTrain equals 'Rear Wheel Drive' then I want you to change the value to 'RWD'
- If the PowerTrain equals 'Front Wheel Drive' then I want you to change the value to 'FWD'

### - 6.3 Write three update statements for the three different conditions 
UPDATE evCars
SET PowerTrain = 'AWD'
WHERE PowerTrain = 'All Wheel Drive';

UPDATE evCars
SET PowerTrain = 'RWD'
WHERE PowerTrain = 'Rear Wheel Drive';

UPDATE evCars
SET PowerTrain = 'FWD'
WHERE PowerTrain = 'Front Wheel Drive';

### - 6.4 Write a query to Select all of the records to view your changes. 
SELECT * FROM evCars;


# SECTION 7 

### - 7.1 Convert the `PriceEuro` to `PriceUSD`
SELECT 
PriceEuro, ROUND(PriceEuro * 0.621371, 2)
FROM evCars;

### - 7.2 Write the Update Statements 
UPDATE evCars
SET PriceEuro = ROUND (PriceEuro * 1.13, 2);

### - 7.3 Rename the Column
ALTER TABLE evCars
RENAME PriceEuro to PriceUSD;