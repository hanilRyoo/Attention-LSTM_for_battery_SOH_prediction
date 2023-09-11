Data Description:
A set of four Li-ion batteries (# 5, 6, 7 and 18) were run through 3 different operational profiles (charge, discharge and impedance) at room temperature. Charging was carried out in a constant current (CC) mode at 1.5A until the battery voltage reached 4.2V and then continued in a constant voltage (CV) mode until the charge current dropped to 20mA. Discharge was carried out at a constant current (CC) level of 2A until the battery voltage fell to 2.7V, 2.5V, 2.2V and 2.5V for batteries 5 6 7 and 18 respectively. Impedance measurement was carried out through an electrochemical impedance spectroscopy (EIS) frequency sweep from 0.1Hz to 5kHz. Repeated charge and discharge cycles result in accelerated aging of the batteries while impedance measurements provide insight into the internal battery parameters that change as aging progresses. The experiments were stopped when the batteries reached end-of-life (EOL) criteria, which was a 30% fade in rated capacity (from 2Ahr to 1.4Ahr). This dataset can be used for the prediction of both remaining charge (for a given discharge cycle) and remaining useful life (RUL).

4개의 Li-ion 배터리 세트(# 5, 6, 7, 18)를 상온에서 3개의 서로 다른 작동 프로파일(충전, 방전 및 임피던스)을 통해 실행하였다.
충전은 전지 전압이 4.2V에 도달할 때까지 1.5A에서 정전류(CC) 모드로 실시한 후 충전 전류가 20mA까지 떨어질 때까지 정전압(CV) 모드로 계속하였다.
전지 5,6, 7 및 18에 대하여 전지 전압이 각각 2.7 V, 2.5 V, 2.2 V, 2.5 V로 떨어질 때까지 2A의 정전류(CC) 수준으로 방전을 실시하였다.
임피던스 측정은 0.1Hz~5kHz의 EIS(Electrochemical Impedance Spectroscopy) 주파수 스위프를 통해 수행되었다. 
반복되는 충전 및 방전 사이클은 배터리의 노화를 가속화하는 반면 임피던스 측정은 노화가 진행됨에 따라 변화하는 내부 배터리 파라미터에 대한 통찰력을 제공한다.
배터리가 정격 용량(2Ahr에서 1.4)의 30% 페이드인 EOL(End-Of-Life) 기준에 도달하면 실험이 중단되었다. 
이 데이터 세트는 남은 전하(지정된 방전 주기 동안)와 남은 유효 수명(RUL)을 모두 예측하는 데 사용될 수 있습니다.

Files:
B0005.mat	Data for Battery #5
B0006.mat	Data for Battery #6
B0007.mat	Data for Battery #7
B0018.mat	Data for Battery #18

Data Structure:
cycle:	top level structure array containing the charge, discharge and impedance operations
	type: 	operation  type, can be charge, discharge or impedance
	ambient_temperature:	ambient temperature (degree C)
	time: 	the date and time of the start of the cycle, in MATLAB  date vector format
	data:	data structure containing the measurements
	   for charge the fields are:
		Voltage_measured: 	Battery terminal voltage (Volts)
		Current_measured:	Battery output current (Amps)
		Temperature_measured: 	Battery temperature (degree C)
		Current_charge:		Current measured at charger (Amps)
		Voltage_charge:		Voltage measured at charger (Volts)
		Time:			Time vector for the cycle (secs)
	   for discharge the fields are:
		Voltage_measured: 	Battery terminal voltage (Volts)
		Current_measured:	Battery output current (Amps)
		Temperature_measured: 	Battery temperature (degree C)
		Current_charge:		Current measured at load (Amps)
		Voltage_charge:		Voltage measured at load (Volts)
		Time:			Time vector for the cycle (secs)
		Capacity:		Battery capacity (Ahr) for discharge till 2.7V 
	   for impedance the fields are:
		Sense_current:		Current in sense branch (Amps)
		Battery_current:	Current in battery branch (Amps)
		Current_ratio:		Ratio of the above currents 
		Battery_impedance:	Battery impedance (Ohms) computed from raw data
		Rectified_impedance:	Calibrated and smoothed battery impedance (Ohms) 
		Re:			Estimated electrolyte resistance (Ohms)
		Rct:			Estimated charge transfer resistance (Ohms)
