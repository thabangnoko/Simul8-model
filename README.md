# Simul8-model
As a group we were contracted by the local regional hospital to make a simulation study of their X-ray department.
There have been complaints about waiting times and evaluate possible changes which might
improve the operations of the department.

# Simulation information
There are 4 radiographers employed in the department. Patients are
either hospital patients (from the wards or out-patient clinics) or casualty (A & E) patients and arrive to the waiting room. Casualty patients
arrive once every 30 mins, distributed as an exponential. Hospital patients arrive once every 9 minutes, on
average, again distributed as an exponential.

<br />Patients are called through, on a first-come-first-served basis, when a vacant X-ray room is available, but
casualty patients have priority at all times. There are 4 X-ray rooms, each equipped with an X-ray machine, a
chair and a bed. ‘Calling through’ can be assumed to take a constant 2 minutes for casualty patients and a
constant 5 minutes for hospital patients. This activity covers the necessary clerical work together with time
for undressing (if required), removal of rings etc.

<br />Each patient is attended by one radiographer. Casualty patients are assumed to take an average of 7 minutes
for this process which is Erlang distributed with a shape parameter of 3. Hospital patients take 3 mins to be
attended, again distributed as an Erlang with shape parameter 3. On completion of the X-ray the patients
return to the waiting area. Those who have undressed are given a dressing gown and carry their clothes.
The X-ray plates are developed by a single machine which can process one film at a time. This takes a constant
5 mins and the time includes a visual check by a radiologist that the developed image is satisfactory (e.g. that
the patient has not moved which would result in a blurred image). If the image is satisfactory the patient can
leave the X-ray department. There is a section on one side of the waiting area which has some screened-off
cubicles to allow those who have undressed to put their clothes back on. This facility, which not all patients
will need, is not required to be included in your model.

<br />A long-term study has shown that 15% of X-rays need to be repeated as the image quality is deemed
unacceptable for diagnostic purposes. Patients in this category are given priority over the same class of patient
being processed for the first time, i.e. for being called through; for being attended by the radiographer; and
for X-ray film processing. However, hospital patients requiring a repeat X-ray are not given priority over ‘first
time’ casualty patients. Assume the times for calling through etc are the same for a repeat X-ray patient as
they are for a ‘first time’ patient.

<br />Radiographers’ lunch breaks and rest periods are negligible and each radiographer is assumed to be idle
when not attending to a patient. Furthermore, the department is assumed to operate continuously 24/7.
