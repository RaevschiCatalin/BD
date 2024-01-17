# Proiect Baza de Date - README

## 1. Descrierea pe scurt a activitatii pentru care se realizeaza proiectul

Proiectul constă în dezvoltarea unui sistem de gestionare a informațiilor medicale, în care pacienții pot programa întâlniri cu medici. Aplicația va permite și gestionarea informațiilor despre pacienți, medici și programări.

## 2. Identificarea dependentelor functionale si aducerea schemei bazei de date cel putin in forma normala BCNF utilizand normalizarea 

Pentru identificarea dependențelor funcționale și aducerea schemei în forma normală BCNF, s-au efectuat analize detaliate și normalizări corespunzătoare. Aceasta asigură o structură optimă a bazei de date.

## 3. Crearea diagramei entitate-relatie (ERD) sau diagramei de tabele corespunzatoare datelor

Am realizat o diagramă entitate-relație (ERD) pentru a vizualiza relațiile dintre diferitele entități din sistem.
<img src="./img/database.drawio.png">

## 4. Definirea tabelelor

### Tabele:

- Tabela `Patients`:

  ![Patients Table](./img/createPatients.png)

- Tabela `Doctors`:

  ![Doctors Table](./img/createDoctors.png)

- Tabela `Appointments`:

  ![Appointments Table](./img/createAppointments.png)

- Tabela `Users`:

  ![Users Table](./img/createUsers.png)

## 5. Confirmarea existentei tabelelor create prin interogarea vederilor din dictionarul datelor; vizualizarea structurii acestora si a constrangerilor aferente

![Proof1](./img/confirm.png)
![Proof2](./img/confirmProof.png)

## 6. Definirea de obiecte ale bazei de date, altele decat tabele: vederi, indecsi; confirmarea existentei obiectelor in dictionarul datelor
### Am creat o vedere pentru a afișa programările viitoare ale pacienților, împreună cu detalii despre aceștia și medicii care îi vor consulta.
![View](./img/createView.png)
### Am verificat existența vederii în dictionarul de date.
![ViewProof](./img/viewProof.png)
### Am creat un index pentru a accelera căutarea programărilor după data acestora.
![Index](./img/createIndex.png)
### Am verificat existența indexului în dictionarul de date.
![IndexProof](./img/proofIndex.png)


## 7. Exemplificare de comenzi de prelucrare asupra datelor: adaugare, modificare, stergere, selectie
### Am adăugat date în tabelele `Patients`, `Doctors`, `Users`, `Appointments`
#### Adăugare date în tabela `Patients`
![Prima adaugate](./img/insert1Patients.png)
![A doua adaugate](./img/insert7Patients.png)
#### Adăugare date în tabela `Users`
![A treia adaugate](./img/insert10Users.png)
#### Adăugare date în tabela `Doctors`
![A patra adaugate](./img/insert3Doctors.png)
#### Adăugare date în tabela `Appointments`
![A cincea adaugate](./img/insert7Appointments.png)

### Modificare date în tabela `Doctors`
![Modificare](./img/updateDoctor.png)
### Ștergere date din tabela `Appointments`
![Ștergere](./img/deleteAppointment.png)

## 8. Selectia datelor - minim 5 interogari complexe ce pot fi incluse si in definitia unor viewuri, care contin conditii/clauze complexe.

1. **Vedere pentru programari viitoare cu detalii despre pacienti si medici:**
![Upcoming Appointments View](./img/futureAppointments.png)

2. **Vedere pentru numarul total de programari pentru fiecare medic:**
![Doctor Appointment Count View](./img/totalAppointmentsNumber.png)

3. **Vedere pentru programarile doctorilor într-o zi specifică:**
![Patients With Multiple Appointments View](./img/totalAppointmentsOnSpecificDate.png)

4. **Interogare pentru a afla pacientii care au programari pe mai multe date:**
 ![Patients With Multiple Dates Query](./img/pacientiCuMaiMulteProgramari.png)

5. **Interogare complexa pentru a obtine detalii despre programarile unui medic specific:**
 ![Doctor Appointments Query](./img/specificDoctorAppointments.png)
