---
subject: "It Depends #35: How big should a method be?"
from: "Kislay Verma <kislay@kislayverma.com>"
to: ""
date: 2021-05-30 07:30:01
labels: ["CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "Kislay Verma"]
label_ids: ["CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "Label_7563788208856972919"]
---
|
Hello Everyone!
Welcome to the 35th edition of It Depends. Hope you are all doing well and staying safe. My apologies for not sending out an edition last weekend - I got caught up with a few things and couldn't make time.
More than one person has reached out to me asking about how to structure code in methods. The question I hear most often is how much to break down a method. So let’s talk about how large a method should be.
Let’s say there’s a method in the codebase that does 4-5 things one after the other. The code for doing all those things is well-written, but the result is a somewhat large method. At what point should you break it up into multiple methods? There is the old adage about every method being fully visible without scrolling which I have always found weird. Let’s try to do better.
The good part about having all of the code inside a single method is that it is all in one place and in a sense, easy to absorb in one shot. The bad is part is that it makes the method large and if split, the reader will have to move in and out of multiple methods to understand what is going on.
I prefer the second approach because smaller methods are easier to understand for me. But there has to be a balance in that direction too. So while the correct answer is obviously “it depends”, I’ll try to give a little more in the way of guiding principles.
The key to writing or refactoring software is to reduce the cognitive load on the reader/maintainer of the code. All other considerations are subservient to that goal (of course, “it depends”). So the key to answering the question of granularity is to identify how people read and understand any piece of code. Or rather, how do we want them to read a piece of code.
Typically people read code from a higher level of abstraction to a lower level of abstraction. The guiding principle of each layer of code, typically represented by methods, is that it should prevent the user from wanting to dig deeper into the next layer. Not in the sense of sending them away screaming as quickly as possible, but rather by making what must be happening underneath so obvious that the reader never feels the need to read the next layer. In the context of this article, cognitive load can manifest in two forms: engagement and curiosity. We don’t want them to feel like they have to think (engagement) to understand something, and we don’t want them to want to think (curiosity) about something. This is sometimes called the “[Principle of least astonishment](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/r2gAFoD6rKrjbJn2U1Oin1jA__pOmPj-PS2UAlbXXOHt8MTefx_vcVcSahswmEWR9DFlMaTwbouekQVOn8CFmtiJkgijTCC4pbAwR_YKNTeaP51GNfao27C9jrA9epVcqn9gRaEmiKH-Lgv7-WCaVR9DbpYNRUixsF2pQVikp8mp_8oofchBJQbpfREnlnNS9op4Ig0uoa19acEvRngg2l8nrGzIHrXssBjtpm8eD1kw1Om_8BSyaWT8ApHMczPeXTHWLYCSGNFyQPcQbtAHcu8LEJnvKuCWeWa0RST5I5N3CoDpmkRAtw_8HpypA28LiMCaSSW4GLvVmacB9KDS3ya4FOSGUiDCQihuWMQA1k-_QbRCLeidOp6GhN1A0XPuvww3RwARE4rmWdqCoSUpug)” and applying this can help us bound the upper and lower granularity of a method.
At each level, a well-written method represents a declarative (what is to be done) unit to work to its higher layers (the ones who called it) and internally contains a set of imperatively defined steps (how is this to be done). In this sense, our method in question which does 4-5 things, is in some sense a workflow. As I wrote in [my previous article on workflows](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/WzWoyE3AmgixjoRY3u0NP_5CsnMPPKLpaUsfcMgCGjAloL6pHZ18tHGQRaM_JjgJMSZmwI0pVWWcdBuNauBoWaDLbpw4cXtCF4_XabzCGXDQzZeC2fv1sH6LMZa2E6I6QAErSNpoMdCuzFkBr-7o4Ap2n_aw4a0wEvcVhCsRkoPVdGyg1SsX39A_V4OAInwLAIb7AZZq0sImIaPYcWtd1Yy_auFwcqgufQ7v8ExC3lt2cLuQu25_XG4dub2vne10pvtWJ7WKD9nUK4jBgm47vDfQth1ZjmoOM88JezI5IBXFPg7LDL73H3M5vQgkasQ7WiE2K5gKidBQozFScvmmZ0nAuDmrRFlKdaUgdsX62M8gk1inaFhFfub1bljVxWyNNcvL6M1I0BhrRiE8swcxBNtBjBqnS1a0XfXFDgWryzmKwzf8S07M0J75B3kbvuyuGbeZ81b8G-M), the place where a workflow is defined should only define what steps are to be taken, not how each of them works internally.
Let’s take the example of booking a doctor’s appointment at a hospital. A makeAppointment(hospitalId, doctorId, patientId, startTime, endTime) method can do several things:
- Check the working hours of the hospital
- Check if the doctor has no other appointment during that time
- Book the appointment
- Notify the doctor of the appointment
- Notify the patient of the appointment
Let implement this by putting all the code in one place ([gist](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/OnIGDzRAjEc8UG8i8iVDN9GuarLa1TWE4mO2L2SdjsBuIGpR7U5j1-nCprcb9JNHibPQDeO7Ke7C4CzdBE93EOIldKMgux3HD1lxlX5HGlPzxUHQiatbVX2MOWSwHvuLwkQGibPTk1e_rfzDGs8ujjigaUhpqdhPHieTLF_BkTxBDy8_jhewcasUaBWGmLXDCOJ9cOiUuUmEZVXt4YFeGdfBzxIevwbjDnbdHYXDSscLVfpY6UQODOVLW_SGzv_TXSx0WWpkKnpREv74Y0tW7AxzxIVW-2vgBE8VduBxPKOqRis4kqpVU--27DOVERC41EWKBVA5m86wNQCXblzQZiazvdp-v_-SkyrHOxfZ3O3uTNVJ0MjG0I8pQs7kI8w72_3H8M2H_6z8ABnN1n2_RNdQ3R7G9li6O_gnj5mqyiIi009KV4k_GVr_KfA3ByFGrtrh_i35X2ZDyqQ5)).
public Slot makeAppointment(Doctor d, Hospital h, Patient p, Date startTime, Date endTime) throws Exception {
// Check if hospital is open during this time period
String hospitalServiceBaseUrl = ConfigReader.readConfigName("hospitalServiceBaseUrl");
HospitalService hospitalService = new HospitalService(hospitalServiceBaseUrl);
DateRange range = hospitalService.getWorkingHours();
if (!range.contains(startTime) || !range.contains(endTime)) {
throw new Exception("Hospital isn't open in this time period");
}
// Check if doctor has no other appointment in this time period
String scheduleServiceBaseUrl = ConfigReader.readConfigName("scheduleServiceBaseUrl");
ScheduleSerivce scheduleService = new ScheduleService(scheduleServiceBaseUrl);
Slot s = scheduleService.getAppointmentSlots(d).stream()
.filter(slot -> !slot.isOccupied()) // Only consider free slots
.filter(slot -> slot.contains(startTime) && slot.contains(endTime)) // Only consider slots which contain this time period
.findFirst();
// Create the appointment
s.setIsOccupied(true);
Slot bookedSlot = scheduleService.bookSlot(d, p, s);
// Notify doctor using custom email template
DoctorEmailTemplate doctorEmailTemplate = new DoctorEmailTemplate(d, p, bookedSlot);
notificationService.notify(d, doctorEmailTemplate);
// Notify patient using custom email template
PatientEmailTemplate patientEmailTemplate = new PatientEmailTemplate(d, p, bookedSlot);
notificationService.notify(p, patientEmailTemplate);
return bookedSlot;
}
This method is not so bad as some real-world code you may have seen. But the moment I reach this method, my brain has to wake up to the details of everything going on here. I wanted to understand how an appointment is booked but suddenly I’ve run into a bunch of API calls and other things. This doesn’t exactly match my [mental model](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/JSyIOc_kTcNqX7-wF97pC4ztUrFpxxLUCfs82VxzUEzk5RyD-dtqbml2rmf_tg33NW38u51cCCZuyJI5fnfbH11FGUbKcWI8wbYoWAUkjDbLRLQeiIU8nIRJsD7B3fzhrAcl7_CYPRVpZ1nw6tl91kj_2GXApnAB4kb0y3SJ4H_sF5QUvBrk9BqK3GU1sfag_oLmlsSLdJr7ko2OCgw3tz8JCzY8i8o20ky_2KtT0KGcj3_E42li2NhT6A8LARo8lyUVmoLx02SATT7kc18ErU_Y3gGSoofKzHUR_PPM8tiRTazQ0g86yQO4_HEGPd1LkhUWZd0sC9iaYOEy7uU-ddZAlL-zEli6-_1qgQeACsqepmgQAMYCxoZrLbByoJemQcbUqidBF1-b73Q9iE-WMeI7p0nBG00n) of how to book an appointment. This result is a high cognitive load. Therefore, this method should be broken down till it reaches the mental model “in English” as much as possible. Here’s a possibility ([gist](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/buhLNZBjzcjSYGNPDrkudN_Bqawme485NsxUk7SOD8JHO6zmmNxnDJ8P1BPywIG04nVwfkEClg1nD0boTj5N_pnOkxjN4b-dG2aBk6ocsFDlPZhOqWXuKtsOdKqbfcbD3Wrjl2NMXDtHSTSeG5J8jZ4jxt0S2Hqy1ZfNqk7kI9Cn66GGzbfLHRc6Ff_ydHHkvw5cwx5LWS5VpgwAEGk6S2wpkuUh2QH4VqR-wSrCu8z8dPZBoUw4mo21H_vVPc-ul9agXxIluDeq-VbgadbhQfgGQ1lcH5MvkD1MhmMEBQUCoX_5tzg1EobEjgJkI7oo8aN_fP-EIxR69cuCPAugYWknpl4Wy4MIHLJQ3sDrza0npDSpkPwP_HHu5SNmpcrgLzuQYbtar8mLR8wb4WP33gOePzA)).
public Slot makeAppointment(Doctor d, Hospital h, Patient p, Date startTime, Date endTime) throws Exception {
if (!isHospitalOpen(h, startTime, endTime)) {
throw new Exception("Hospital isn't open in this time period");
}
Slot s = getFreeSlotForDoctor(d, startTime, endTime);
if (s == null) {
throw new Exception("Doctor is not free in this time period");
}
Slot bookedSlot = createAppointment(s, d, p);
notifyDoctor(bookedSlot, d, p);
notifyPatient(bookedSlot, d, p);
return bookedSlot;
}
private boolean isHospitalOpen(Hospital h, Date startTime, Date endTime) {
String hospitalServiceBaseUrl = ConfigReader.readConfigName("hospitalServiceBaseUrl");
HospitalService hospitalService = new HospitalService(hospitalServiceBaseUrl);
DateRange range = hospitalService.getWorkingHours();
return range.contains(startTime) && range.contains(endTime);
}
private boolean getFreeSlotForDoctor(Doctor d, Date startTime, Date endTime) {
String scheduleServiceBaseUrl = ConfigReader.readConfigName("scheduleServiceBaseUrl");
ScheduleSerivce scheduleService = new ScheduleService(scheduleServiceBaseUrl);
return scheduleService.getAppointmentSlots(d).stream().filter(slot -> !slot.isOccupied) // Only consider free slots
.filter(slot -> slot.contains(startTime) && slot.contains(endTime)) // Only consider slots which contain this time period
.findFirst();
}
private Slot createAppointment(Slot s, Doctor d, Patient p) {
String appointmentServiceBaseUrl = ConfigReader.readConfigName("appointmentServiceBaseUrl");
AppointmentService appointmentService = new AppointmentService(appointmentServiceBaseUrl);
s.setIsOccupied(true);
return appointmentService.bookSlot(d, p, s);
}
private void notifyDoctor(Slot s, Doctor d, Patient p) {
DoctorEmailTemplate doctorEmailTemplate = new DoctorEmailTemplate(d, p, bookedSlot);
notificationService.notify(d, doctorEmailTemplate);
}
private void notifyPatient(Slot s, Doctor d, Patient p) {
PatientEmailTemplate patientEmailTemplate = new PatientEmailTemplate(d, p, bookedSlot);
notificationService.notify(p, patientEmailTemplate);
}
This looks a lot more like the workflow I was expecting. The details of each of the steps are now hidden, which means that they can change without us knowing about that. But the biggest thing is that I don’t feel like I have to go into each of the new methods to see what they do if all I want is a logical understanding of how appointments are booked. There are technical things like exceptions that still intrude upon the reading experience, but for the most part, astonishment has been eliminated by reducing the model-code gap.
Now let’s go one step deeper and further break down the methods here ([gist](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/A2eOyURAN2vTc-qv1JCtAyApw_7fy-MNiF6Bf-MbKDwT534hBMGMzze3-QJPzSBLwPvchoe9Mdbo5T8TJf_eEhxwbCE9mCBn5eQC6aR_uMk8xaYnHAAuYARz_gQEnaFXQSTA4gqq9FqUJjOLBx3N7JlWg57GTp2snwtr2HxfNHaVYPINwGBwTzhfxRFdgy5SRt00843zwL3VEu-8oL7nR3eu5uHaoUBCOfn6jiTvaKmNHMVq5xg6BV0upXHy6TSC6uB4Q25quueCOB7TT2glDghnsdGoN-rc6h6A1rTf21FZizs7HgIycL7BJEyRn8ZqdKHdrt6dRTYquugBsMVkLWeEOGccbNLiYRKdxL8Tsnc1fxSQqKYxqMG11FMbKhKJwCZrKNyPwBZbZGL8St5YXp7SI2Q)).
public Slot makeAppointment(Doctor d, Hospital h, Patient p, Date startTime, Date endTime) throws Exception {
if (!isHospitalOpen(h, startTime, endTime)) {
throw new Exception("Hospital isn't open in this time period");
}
Slot s = getFreeSlotForDoctor(d, startTime, endTime);
if (s == null) {
throw new Exception("Doctor is not free in this time period");
}
Slot bookedSlot = createAppointment(s, d, p);
notifyDoctor(bookedSlot, d, p);
notifyPatient(bookedSlot, d, p);
return bookedSlot;
}
private boolean isHospitalOpen(Hospital h, Date startTime, Date endTime) {
String hospitalServiceBaseUrl = ConfigReader.readConfigName("hospitalServiceBaseUrl");
HospitalService hospitalService = new HospitalService(hospitalServiceBaseUrl);
DateRange range = hospitalService.getWorkingHours();
return range.contains(startTime) && range.contains(endTime);
}
private boolean getFreeSlotForDoctor(Doctor d, Date startTime, Date endTime) {
return buildScheduleService().getAppointmentSlots(d).stream().filter(slot -> !slot.isOccupied) // Only consider free slots
.filter(slot -> slot.contains(startTime) && slot.contains(endTime)) // Only consider slots which contain this time period
.findFirst();
}
private ScheduleService buildScheduleService() {
String scheduleServiceBaseUrl = ConfigReader.readConfigName("scheduleServiceBaseUrl");
return new ScheduleService(scheduleServiceBaseUrl);
}
private Slot createAppointment(Slot s, Doctor d, Patient p) {
String appointmentServiceBaseUrl = ConfigReader.readConfigName("appointmentServiceBaseUrl");
AppointmentService appointmentService = new AppointmentService(appointmentServiceBaseUrl);
s.setIsOccupied(true);
return appointmentService.bookSlot(d, p, s);
}
private void notifyDoctor(Slot s, Doctor d, Patient p) {
DoctorEmailTemplate doctorEmailTemplate = new DoctorEmailTemplate(d, p, bookedSlot);
notificationService.notify(d, doctorEmailTemplate);
}
private void notifyPatient(Slot s, Doctor d, Patient p) {
PatientEmailTemplate patientEmailTemplate = new PatientEmailTemplate(d, p, bookedSlot);
notificationService.notify(p, patientEmailTemplate);
}
Note the buildScheduleService method. If I really want to understand how ScheduleService is invoked to get a doctor’s schedule, this still looks all right, although just about at this stage someone will start arguing that service creation should not be done in this class or that it can be more generically for all service. That’s fine, it can still stand alone as a method, if not in this class then elsewhere. But the question indicates the curiousity/astonishment quotient has started rising.
Let’s take it one step further ([gist](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/BWCXlKWJ7ZaMaGA9Rmd_fas5x7FbpdSXtgFvpYB2vmTZTWT33622cWCdKZgtL3fzawD6z2BAkJoh1LUNv1Z3n8rTpe0tYATzLBzv0N9oZnpe2-co8uA-CiOTRWQbwpqLNTB9lMwrNQI7Pvd95N57WM_68O79y0QyacLWO1Xw9yAK3319mhleQI-MAouuGjbqnV23KGRykOZWCARYxmAdJGM0Y0shJZvKrSYWkPvay-FU8N1sqw-4TxQ2PtosUqSEwjxY1uFOYp9875rFZF_lVIFGseHkrvks5cfpU5AxzeTzwdBdCxvb6cjuWTdBff_KXyxrBiN9zU-jOFkT9ioyXfTCeOApbB4uUH-vCCmVf0xo90BtVR9OMqdI75bPLTGeNj6rsPBpL3dIVEgbiENTkYsA-7A)).
public Slot makeAppointment(Doctor d, Hospital h, Patient p, Date startTime, Date endTime) throws Exception {
if (!isHospitalOpen(h, startTime, endTime)) {
throwException("Hospital isn't open in this time period");
}
Slot s = getFreeSlotForDoctor(d, startTime, endTime);
if (s == null) {
throwException("Doctor is not free in this time period");
}
Slot bookedSlot = createAppointment(s, d, p);
notifyDoctor(bookedSlot, d, p);
notifyPatient(bookedSlot, d, p);
return bookedSlot;
}
private void throwException(String message) throws Exception{
throw new Exception(message);
}
private boolean isHospitalOpen(Hospital h, Date startTime, Date endTime) {
String hospitalServiceBaseUrl = ConfigReader.readConfigName("hospitalServiceBaseUrl");
HospitalService hospitalService = new HospitalService(hospitalServiceBaseUrl);
DateRange range = hospitalService.getWorkingHours();
return range.contains(startTime) && range.contains(endTime);
}
private boolean getFreeSlotForDoctor(Doctor d, Date startTime, Date endTime) {
return buildScheduleService.getAppointmentSlots(d).stream().filter(slot -> !slot.isOccupied) // Only consider free slots
.filter(slot -> slot.contains(startTime) && slot.contains(endTime)) // Only consider slots which contain this time period
.findFirst();
}
private ScheduleService buildScheduleService() {
String scheduleServiceBaseUrl = ConfigReader.readConfigName("scheduleServiceBaseUrl");
return new ScheduleService(scheduleServiceBaseUrl);
}
private Slot createAppointment(Slot s, Doctor d, Patient p) {
String appointmentServiceBaseUrl = ConfigReader.readConfigName("appointmentServiceBaseUrl");
AppointmentService appointmentService = new AppointmentService(appointmentServiceBaseUrl);
s.setIsOccupied(true);
return appointmentService.bookSlot(d, p, s);
}
private void notifyDoctor(Slot s, Doctor d, Patient p) {
DoctorEmailTemplate doctorEmailTemplate = new DoctorEmailTemplate(d, p, bookedSlot);
notificationService.notify(d, doctorEmailTemplate);
}
private void notifyPatient(Slot s, Doctor d, Patient p) {
PatientEmailTemplate patientEmailTemplate = new PatientEmailTemplate(d, p, bookedSlot);
notificationService.notify(p, patientEmailTemplate);
}
Any developer with any amount of experience in any codebase will get curious as to why we need a separate method just to throw an exception. They will try to go to the lower level to understand it, which is exactly what we set out to prevent. At this level of granularity, our method size is causing astonishment so we should abort this step.
The point at which engagement or curiousity begins to rise depends on the business and technical context of a codebase. So while this is obviously a simple example, preventing cognitive load is widely applicable as a guiding principle in software engineering. When reading a piece of code, keep in mind your engagement and curiousity levels. If either increase, there may be the possibility of refactoring.
From the internet this week
- Ingrid writes about
[why decentralised applications don't work](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/vrYRdr-GNUAvAGYPJHCwFIjcLYjje5tyBrDDHFlcZnnvtzeXZ5YEmvfPEmznnG1dApCHWZaFAnrB4vdXbSioIxEGLsbwY4zrL2McCoRMyWEh7b_-Wqwisfs1uGynovKBK_MQGQHdchU4vhy9vrpK4j91lPzJ79peubITPZdyvavboZ-F_zHLfrPHdHDvUxl0hoZjZFzT7eUfyPI8gfL73qr9aXFzBbwJrPAISBg3FMDGXHHyUl2xYIQoYhYRQYT1wKtmG_XBSZypZ3DAPVWzGF1QhlpwkQSPmmoJkYc-oZOIzSYq4m-xDULIKV_nTDwhvVFt5HjZ0_Mzb82IeCFt9J1fXZF732f3ix-dWKwqTBj0Mj4nAfgM6z9c181itATB054iVLQStqt0raD-) in the real world. With crypto making news for all kinds of reasons, this is a thought-provoking take.
- Here's an old video of
[Brian Kerninghan interviewing Ken Thompson](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/nF_LLqqYfESheuZ3qj_2qOSSBAdl3fgphOLxhY6NQxrwUpVRIy9ek0Q084FmuYckqPEVanwWLdPYh5UPwE0TCr1jxa0q0_0mfjdaxCkHaiqxA1aVHSxnF2hnSZiyUIjkqp26g9EB5yVgkfAGJWM69cDUmqsbH2tl_IAQeUj8P446o7AsY7iXTdIgi6vtgkpRP_3PcuLxkbf44XfONR3hXLDCtA-Cel7v7euHhMkkERNj6smY8q5CwozvJwhv5p8VQ1mztaH8yi86esTny6WHI56fedTI0YqC-FRsJTIvg1sV9-P1vIbUYzSAqxEMmuQuFbSzexmsXcWw92ePY9HNgIiSqpz2Qo5Np4JZ6yTT5sso0iBN). The interaction between these two greats is worth listening to.
[Jamie Brandon](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/NrCDBDFdX662WcOqZjq___1e-kXLuRzzupvsDhQqyCPKEfk3fBCiMNJAZKdvSGGfTLwvWumZupQXexZLY8VQOeF4T2R3jGVv5ly7nM-JyKgU1kd1Rh4N4TzOOYcQATvjnb6uJq0z0WQdtUWFEF0Bw-I0ckTw_3o1KDKOF7E5joMmN8-773x4NrcQRoxM9CAcPiZv02Qs9l_AtdOK7vfC1NjN52y6oOLMHr7SJVgfrr3c8SCWcMuIFvyWHMr2FPJRf1n0Z56ODXuQQqC8ZBYlbyWOL1sxs6e9S5RTRMBcKOdM9VnKry1m0wwB5TY6eaOfH1HgwY-oZaIPBsOm) discusses [consistency in streaming systems](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/-yzXL3XXCKm8iIOTBaw2FMfLRKIP3Yh_Wa16KAXo0XbJTo7glb2CjVtpRNxcrYOqMN4SNzMiGyOW_mrzKkLTRgolbzIfxW-jRDeJOj3nwQNmkjv1JAOacqxlrYySXZ9ZJqSPc64-C2KY32Pa2KoYahUg_zRFvHieA2sZYDXbMo0WhB0mqVSCCrZID2Vr8p6vTzeIK4qrd4bGbGpmltquhk17HMYrmqH9OQcbTvy6oOIh166tPE2c54OzfU_R242TEC4-IYsD-osu-078H5Gg_C7QEksnm66hKQG9GDXDuwpz5qy2z6WU-476Nwv_Wcafh-xfl-xqp66dd2PBsJkMjKhIOXXr6PTV3mWUfz3Q0k1LenGb0V8XOxcbF0_C_5R0anCZvk9uaS4Kzds_aSm_MGYTh3-UlORLJxy_ARZr5lE).
- Our words shape our perspectives.
[Sarah Drasner](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/g0x6KeSjFYcZKgW_SzQXbfs_WVKVIy1LP74_bnVz5g09l-zz7x2Pyc_iORRZVDIKPaVIeXz-BvXzfYc1-Fp6G8VsUTdtdrY6Oa8lPOL21WAXfo2FxUcsMhZN-r0zq7aH6QsyAn8P2lUUywLNqf0GIydBD0g5CmftzLvL6dpANAEbem3H2MW_OwNTzdPcWboAj62gtYDHs9zc2ynkzig_X83t08TZhSUEEn1Qen7EVYBBGy5QhalCYLH84OnroS0pl5_tXRg7CKJgL13QJFGengBH3jLTf3U2a08uEW-w_fgE3J05R8Rs0s8E6yJDQ00QjCu06-yqdEzN0vaQ8Wq7GA) reminds us that engineering managers should think of their team as ["us", not "them"](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/fZTqSywyR3szPQWKiBPtvDCc0A81K3CuZ3eDoKgJGnOhnOb9CXabSYLzVjVLFK4Buhel1wVGn11QIPxcHQNocUcOurSMSK92V5PJghRcSjJoJ9oln54HHWB6xEMy5uKq2DVORjAkfzXiz6t7txWU5OD5Bs26g-tjEMVQBZsphj0OdVI16i33QakQCzc3vbbBk5xObrtba1k7jrtj76fJOjv6708iFcQp1KoMT2LYp_jFLoB9-P-MI3TVg0VGnhTfPpUYr-Rb5emndorzOHw42NGb36XHgt3aCOkS47o_slUBzwnroq0IAdfj_wEtLPzGhvlcixE7c1OuXwsQl81faihuTcClLdv0Il4fOrg42Zc).
That's it for this week folks!
Cheers!
Kislay |