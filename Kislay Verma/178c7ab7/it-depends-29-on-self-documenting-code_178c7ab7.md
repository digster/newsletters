---
subject: "It Depends #29: On self documenting code"
from: "Kislay Verma <kislay@kislayverma.com>"
to: ""
date: 2021-04-11 06:40:30
labels: ["CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "Kislay Verma"]
label_ids: ["CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "Label_7563788208856972919"]
---
|
Hello everyone!
Apologies to my regular readers for the 2 weeks break. I had travelled to my parents’ place in Delhi and there got involved in a false-alarm COVID episode. All is well, and I welcome you to the 29th edition of It Depends. Today I will talk about self-documenting code (you can read the article on the website if you’d like), followed by the usual awesome from the internet.
I love documenting code and systems. Many don't. A major argument against documents is that they get outdated as the system evolves. And the faster a system evolves, the faster its documentation gets outdated. Ironically, this is the very type of system which needs the most up-to-date documentation!
An argument is often made, therefore, for self-documenting code. This is ostensibly the kind of code that doesn't need separate documentation because it is designed and implemented in such a way as to be self-explanatory to the reader.
How does anyone reading a codebase understand it? First, they need to know what the code is "supposed to do". Then they can graduate to figuring out how it does that. And this is where the problem of self-documenting code lies. Because reading code is essentially reading the how. "Query some things from a database table and process them into a map, match them against some other things from some other table, and return everything that does not match as a list". [Well-written code makes it simple to understand how it is doing something](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/1HU9-4g5tHlPaIUpYP47B0YvH_B5yKMB_asKAD2FNyewEJ30AfHtw0enMAz31ECWt_n02d8osfmW5kS3RRy_2yGj_CG-hpzPzvhgG92rbL6rfAcx2VYEbBltUElHyMKCyALu2LmkNQfaYgk_EUV-thSboAR3Neebbvi8USCJuHjPBi03W-sHYw4dKqxBq0loQJsbYqdlXmdlMJPMDxne-jeKvp-pFbLW3diNQKhCTKk4N4Jrz6-vPSBPdQGRpOjxmkU0D-5wZrFybyKDAoepfQp91TqPBPuwaiseQksbUNylrc1Da4AJ2AV0BGrXtY6ZX4GMkXRTERK3UQYQuEdaXBZClJtnyvLKdl3sMB6m2WgV9SWzVyQ0Qmd96xNvRpMMzfBW37hy23RZPto6yGxLGqcfKa5cWGKZt1pbDw). But it doesn't tell the reader why it is doing what it is doing. And hence the reader remains confused and documentation becomes necessary to understand the intent behind the system design.
So what kind of code would reveal, even in some limited way, why it does things the way it does them?
I want to talk about the only way (IMO) code can explain itself to readers and hence become self-documenting. Let's discuss the model underlying the code.
Becoming self-documenting
Before code comes the conceptual model that the code is the physical manifestation of. This is the mental model of the problem and the solution. This may be the domain model or another specific way of representing the programmer's thought process and how it will achieve a programmatic solution to the problem at hand.
The model is the core of low-level system design. It defines the things that we are working with, what their nature is, and what role they play in solving the problem at hand. The model must be developed first before any other aspects of the low-level design like APIs, data stores, data flows can be determined. These are physical forms of the things conceptualized in the model – ways to make the model “run”. The model itself is the why, and the code is the how.
The only way to make the code self-documenting is to make the code reveal the model underlying it.
This is why the only way to make the code self-documenting is to make the code reveal the model underlying it. Code that highlights the core model instead of hiding it in implementation details builds [a narrative that is much more accessible](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/i9cqd6Te2tqHPP5JQOfWhINjXbthQbLLPdbIxapMlsPmDvgGBhRik47bl_73hgb0JWFIRXScPnQE6JAzshjDFEKdEYsdKsNWpL--tX4QNg1q7onX74r0HFe5TO_Ww11TDPM8S1shD6cixdUA2jP3C1Za5J0Az4CGo1FnNgKNK2KKnTzgR101x9LBlKN35Sv8WDYtm6YdHcmw-yZUJY_0p-K8nSgQ-K0oo8fst1KBWTFr8-BU8SKLEO1RiFw969XC_MgrQB-_RbWtzgRAy0sB8BuOldGg2SQTl9gsO_eRS8VyYGJPwRM1BSe1kyswCQbNOwu6v-ci514pz0YozAZISUJoyAyF0Zc9c2U8yoKyhe3VsFjdNPAJBqNjBJSSflKBYftgfwZlJlL24If6GnUA6KgItKyNBc40YumqQT-mrEogmjWFEB2-Xu_Hw1A) than trying to infer the meaning of some lines in code. The lines can always be interpreted, but the model made evident in well-written code sets the context under which those lines of code make sense.
Let’s take an oversimplified version of Airbnb booking. In the object-oriented, REST-ful world, the code to update a booking might look something like this. (See [this gist](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/-RvIrP8jLiZJo52NjGafm0a2lGgVNFTH52WkbJu5nTENjYft24ZdOsCHrg7yZUY_HFQS46_QWtxjJqqPSpXea8sHcIvkc3Ow5K0nIWqb64EfLcznKB1icgUQnYTSasNBABQ3Nr7JWI9IK0xVlYqheOYWYdSNfXIrTGR2sqi3kzMOqANznVbqwHBaU1YUfckfvEE6E1m9ibpBAi5YDA0o2gg6XtV9mBuc4BYr3s_TPARbcmKhPz7nv8Dme2LqUxwPLdNMTzr0mByqxloQ6Epvw0eER5ksSPx_jdn9WAMwwhV1H_d386MB5c_fYWjNJ54Oce3yZOFFsAhUJhh4SOZmSgtyRXvLwfXMz8wMTCcswHh0s1T4PGn4xAEcDAT2yyhriPQYluGO2ebt4DZwwO9EoUq7HT8) if you have disabled JS).
public class Booking {
String uniqueId;
User guest;
User host;
Date bookingTime;
Date confirmationTime;
Date cancellationTime;
Status status; //PENDING, CONFIRMED, CANCELLED_BY_GUEST, CANCELLED_BY_HOST
User lastUpdatedBy;
}
public class BookingUpdateRequest {
Date updateTime;
Booking updatedBooking;
}
// In Booking Service
public void updateBooking(BookingUpdateRequest request) {
Booking originalBooking = readFromDB(request.updatedBooking.uniqueId);
if ((originalBooking.status == PENDING || originalBooking.status == CONFIRMED) &&
(request.updatedBooking.status == CANCELLED_BY_GUEST)) {
originalBooking.lastUpdatedBy = originalBooking.guest;
originalBooking.cancellationTime = request.updateTime
// Trigger notification to host
// Trigger refund if payment was taken
} else if ((originalBooking.status == PENDING || originalBooking.status == CONFIRMED) &&
(request.updatedBooking.status == CANCELLED_BY_HOST)) {
originalBooking.lastUpdatedBy = originalBooking.host;
// Trigger notification to guest
// Trigger refund if payment was taken
}
// else if ........ more conditions to handle other combinations of new/old variables
}
This type of generic update code is fairly common. To me, this doesn’t explain why things are happening the way they are happening. Did we miss any cases? While this code can be refactored to a much cleaner form, but it does not reveal why things are happening in this way.
Let’s consider an alternative (See [this gist](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/I58xPerxnUlfr92Uskw7kKUkRu6qFtDRnS6lUv5CdWsZ3E_0_JZrxKWuOlpNwRgvbFEl38LudvA9JzNdk2avD1V42iwsy0VQMmq7Tw6TVwmrrdsAg5eoPbPsgXQPdUfoJfG05h0y62dV6h5FPvm1f3FESXBO3bmri2sms6liFtVwKP8BuYZvSL0g6Su3svR3296lFEfkgP0DQSk62oeF1XU-xrTa2zUXXlS_hi7T49ss2Gq0teWYF1EpwtEYr7Xlrv7KST_GNomsts4z9li9HJF86AWxAgk2lGAemuPh325InLJkC5NGzjuM7C0ZroKypv3A3PKGg2PSUMQZ4bIfCeKkc71k7ekrXZQwcTp3hF_LmL41uA3nqBPpMxHaATd0wfjBHZa8-td1klvaKfsPa4rTzag) if you have disabled JS).
public class Booking {
String uniqueId;
User guest;
User host;
Date bookingTime;
Date confirmationTime;
Date cancellationTime;
Status status; //PENDING, CONFIRMED, CANCELLED_BY_GUEST, CANCELLED_BY_HOST
User lastUpdatedBy;
}
// In Booking Service
public void cancelBookingByGuest(String bookingId, Date cancellationTime) {
Booking originalBooking = readFromDB(bookingId);
originalBooking.lastUpdatedBy = originalBooking.guest;
originalBooking.cancellationTime = cancelltaionTime;
originalBooking.status = CANCELLED_BY_GUEST;
// Trigger notification to host
// Trigger refund if payment was taken
updateInDB(originalBooking);
}
public void cancelBookingByHost(String bookingId, Date cancellationTime) {
Booking originalBooking = readFromDB(bookingId);
originalBooking.lastUpdatedBy = originalBooking.host;
originalBooking.cancellationTime = cancellationTime;
originalBooking.status = CANCELLED_BY_HOST;
// Trigger notification to guest
// Trigger refund if payment was taken
updateInDB(originalBooking);
}
// Other APIs to handle combinations of new/old variables...
Or perhaps this (See [this gist](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/EMpwAIBeb5Mcaxvx4J-22o1pOvklT51TW6dwTCCE62GtOBBbiWBOloWco9h_tr1Btbjm7hLorjCXbyD871wF7nNuDDOoexdKJuqAH_XS338aU9hFPU-1lDhiwnGpdinI02Wgox5iEYxZxtmwqKGmsQmL9xih8h4SvS2sQco6CzX5MHyzkXRIk3NMA82rIFFikhtGr53Hm-PAU6JseDWrAEA0DGwLOv_cqFvrQQQr5DbKeuYmJJmiqyEpQG9XJusmYQdGxwPrfYQ8M9ATPTbB_drkfyZc7wc30zXxUv9OAjPriD1AJXRna4N_aq869tCuXGLJvK9pp9-qDRuFHe2IcBUrNDpqggbaZifENcODbjCMF1wtOVzwnDdc0sW2yIzE-0EhDtpL0MJ353Sgli3lx-pmZ54) if you have disabled JS).
public class Booking {
String uniqueId;
User guest;
User host;
Date bookingTime;
Date confirmationTime;
Date cancellationTime;
Status status; //PENDING, CONFIRMED, CANCELLED_BY_GUEST, CANCELLED_BY_HOST
User lastUpdatedBy;
}
public class BookingUpdateRequest {
AllowedActionOnBooking action;
Date updateTime;
Booking updatedBooking;
}
// Explicitly define the ways of modiying the Booking entity
public enum AllowedActionOnBooking {
GUEST_CANCELLATION,
HOST_CANCELLATION,
CONFIRM,
DATE_CHANGE
}
// In Booking Service
public void updateBooking(BookingUpdateRequest request) {
Booking originalBooking = readFromDB(request.updatedBooking.uniqueId);
switch (request.action) {
case GUEST_CANCELLATION:
handleGuestCancellationRequest(originalBooking, request);
break;
case HOST_CANCELLATION:
handleHostCancellationRequest(originalBooking, request);
break;
case CONFIRM:
handleConfirmationRequest(originalBooking, request);
break;
case DATE_CHANGE:
handleDateChangeRequest(originalBooking, request);
break;
default: throw new Exception("Unhandled action on booking");
}
}
// Or move all these private methods to their own handler simplifying this class further
private void handleGuestCancellationRequest(Booking originalBooking, BookingUpdateRequest request) {
originalBooking.lastUpdatedBy = originalBooking.guest;
originalBooking.cancellationTime = cancelltaionTime;
originalBooking.status = CANCELLED_BY_GUEST;
// Trigger notification to host
// Trigger refund if payment was taken
updateInDB(originalBooking);
}
private void handleHostCancellationRequest(Booking originalBooking, BookingUpdateRequest request) {
originalBooking.lastUpdatedBy = originalBooking.host;
originalBooking.cancellationTime = cancelltaionTime;
originalBooking.status = CANCELLED_BY_HOST;
// Trigger notification to guest
// Trigger refund if payment was taken
updateInDB(originalBooking);
}
private void handleConfirmationRequest(Booking originalBooking, BookingUpdateRequest request) {
// Business logic
}
private void handleDateChangeRequest(Booking originalBooking, BookingUpdateRequest request) {
// Business logic
}
What is the difference?
Looking at these examples makes it obvious how we can write code that makes the conceptual model explicit and hence reduce the cognitive load on the reader. The way to do this is via abstractions. All code is likely to have some amount of abstractions, but not all abstractions surface the thought process behind the code. Often developers use the model abstractions only as data carriers without imbuing them with any behavioural or semantic significance. This is the case in the first example of the generic update API. The Booking abstraction merely carries the data, all meaning is encapsulated in the if-else conditions.
Model-Driven code, on the other hand, uses model abstractions to represent the core elements and uses them as the building blocks of all other interactions in the system. They are the heart of the system and all other code only manipulates them in ways defined and controlled by the model itself. This is the case in both the second and the third examples.
It is not the case that the code in the first example does not have a model underlying it. Much like it is not possible to have “no design” (there is always design, even if inadvertent and poor), it is not possible to have “no model”. The solution sitting in the developer’s head is the model. The first example just chooses to obscure it while the latter two make efforts to make it clear.
I hope this has made clear the benefits of explicitly using a conceptual model, and building the system around it. This won’t make the system (especially a large system) automatically self-evident, but it does go a long way in that direction.
From the internet this week
[Manuel Pais](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/xE3jnFsDZZ8O4J5v0XSSeAFZSz_BI20RQJbyH8wPUIHYXniteig-ly3W6KhLApWAyYrg49qmLnT59vikehkSZpLATGXyN6TSMpSWg3fMdaN1aiRgS1lsWkvZbQR5ST0Of615nfOBlY82gjwwOgyf-CKDvcjw_0NRHBs5yZCmQZGVgHQ2nVnyMggD1LvqjjG_POsPNV9YWgYMqbKwFocUaCwL4kRFZ6f9ZM_vW0ozJR3mreg1B94TdlYP0qOa7ny75ludRLW8D9yCB9i3owWkofV_N6HdAR-hZGkakV-Q6nhNDdCCEs-TH3D5IfqpGoXVgXnGbR2GfoUA2a9IwsEGbxNKzyM) and [Matthew Skelton](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/qGswlzeopK89A3HhOVyn8b7sC-xrVyqFHdLSpsF6-ekGfW4GiuVjAH-azx3y-HSdiccM8Zavpb5gh8TCxpn28X_HPa9E6S6SWnKW1tJ-hjGQteEy2esbXWZJRcgH0Drv3_x34UOZu6zQ-2EYMk3jyEorzjvqNmjJ_nDFE1n8eRGKnRirBB-_co7Bta2ZLGNYiMhVB9lon6HmBeseoW2etIvLIBYAzM0_StN9iYq_o5cZqX3idjACPJWc-9M3AHd-1NzhOrj25HH4oe_Eq9z3NNVNvBEgoAS3zBM0SJ2LE8JrjPAquiJ8zuG8zVvJXQJXwlYKh93QtghYic5rImEigewlrPdM--N3) reiterate their focus on “team cognitive load” in this [talk on monoliths and microservices](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/KXf66qLcLcKxAie_1RhDs578gMTXrhe_l2uJzWZF13v8gvrGa4VFOwjffI8v_NIr9OoId5bbGzgXIFiS1waFVxje0_blSmM3wgQakh_ulhRbv8G1-jg9kaElfAze113hZbFRRG8IipTIqPSDfHMnWBI3a5_W73oeWkrOmWllwN5flNXP-KuB8xcSFj218rMt2KYuVQQaHyrBQwOya8MKB-fadbvYGXkhzOKIyBkpD69LYSzTPLRldcSlUd8orhjSn_pOIh25isFyw8YArLMSA0XO63RdblaiWXpbgXESNOw6dyoc4g7o0XUnMYISUET5XxjYDcjQw8Ar7OU4GIDhB7541DQVvdtM4RC2JoaDCZzPW2gNvUhF5g). Their book [Team Topologies](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/se_3NCYiEy8-14zBtp28kBj5ZiAPRz59SiywH6bySfyOKEUdN3kPFzqxsx8GjMoFxhu7nm5KvwCEmnrhI4gByyIMXcazUVzbxLy43aRnfZvo-uiLEcy0s7FVX46riG42JF3BlKRjHQUjUhSUgCXtUKFDg2GkaT0MPf7N-yEbuUJmf0myyVeWQjGeYKVbCEl7orcpVPkI9azMkv1qC730r_2gtd8jE0nZUcf8df2pcQ0PXXXuHG7c12enLUul_MdqQkMSrPCF4Cd6XWmNMNWsuekmvqgVoceD1T443sVMLe18ZmUVmhRdsZEFRs2F2Q6heKYc0ZUXQH6diRHfjXR7GlMm3X1lh_WeSFXH-_1IltYjfTjM6Z-imuptt37p8Q5yTCdawkPHR39zuncVRdev7jndFLk2P5Vl_RJEN4JTglsevvXqbiIFpVRgjZ89hw_LI3dfsIT_qmeVhtiZpHprmBNv9sUxce0EgX8gUGGTmOw) is a must-read - get it NOW if you haven’t already.
- Two book recommendations in one edition - that’s a first for this newsletter.
[Steps to an ecology of the Mind by Gregory Bateson](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/kI1N-uWiwbLWkwQy7YPj9GO1ZfnZHD7rm4KPVhPqH3rQEYiZ1KjOEJ9t2mCE7SrmQqUVc7ZGDm85cUwcmowcfCjdNWssWUlVniUiKo9QKL0b-ibu-Yyb3rfHcbL3w4blG8OBbAf5V-p2lIVT411LTkhv0QZg67qvZW9ndyXpxEO_g8r_Kdt5AHiYru5kLro4aRwnrpoClJ4sXgIH1KV2p8PlxjTmiWzc0SPfDLPyYbfHhvduI7JPwxBgwWvGZ-2nljlaQSp21YN6KjYdJ47_oGPe0UjmlQHqrMD-RPS81mZ0bDexufADOp20Df0TaWEVluJJ2mZbJlqa8QgjGuvL_dKqI1Gph8y1ehkHl_0YE_FMjSwy38DXF830pLTG1IQykHUSJezG5Ulexk-aEzeXlxYredZbu3VH0ziZdWl2Mtl9Oq3brXSHLyfzzKRwzB2oDOeP1bvteZxx0ZH0rtBmCyjKEV9BBPghZALK8DwFWJCM_vky) sheds fascinating light on how computing was expected to evolve. For audio fans, here’s [a sample in the author’s own voice](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/XmyRkirPZq0z4aB9KTODyrlQJz7oX_iz0eewp1uqkTs1xFOzkgilnPgPZP-cb1C6_VSeKR69vBq-DaZrzFT1uvC7F1q1DUmIE761eYCT3h8OD_PfI-ZJ4svwLMOUmUi4CyJfxm0rglptPI5df39LLW3Z376131wi9sGeIYztdZ0pu6nBaR3F0MvmdAIkBPgLM6rufrpt4iIf1O5qGuNaxtGVh6uxO7ugvxoBwiHPB0hvTEQzZWBO6Zew9UpBx5D7MT2MSjyl_PQfYd3eJwyLuqoWz-M37HrM88L31_jN5e5KoOfKVUZdM7rDlypdmwFHeVyDKX_hFHorzOxx298C2Sncggu96As7iYitq8xZ2-OscxPW3BuUjFTYvmsPmkTUMI3vvMWy6TLiCxjs6oaTcJTqhvk).
[Javier Ramos](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/Yh9Q8pkHHiw0ycbJA8pkHnCtKtvD1hEYBalrDtfQId5xo0DTlP1Pu1bN_6vrZ3Y6kmxjSU_5Ho7itTTzXKFshllVoDlWpepef_98UymWlvgvv6pHLp9Arnmo70Dys2M6FoMJjuvaAYd3dIU8f7TkDynCcXSxgex7l3RIa2G8AOCatwknMRnBChSbRGjcIS3TQkN62pgJkZBuh3x68sVb_JeSwNwOjlpeoJxuAVx0EhjmUMwZXj2hsDvH47wXos-WEM0IZYzI4dzdePt6KMzlakIqJ-KnU7OsHIhlGLnGol8z55T6ZpcmYQAZLGtoSrKb9WmbyRTOB-gAmuK6YvRlN58bhyhIS_mI5hiS2A) has written a good [comparison between Pulsar and Kafka](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/SzSE4m7txfO6BxCeSA4rw-CGyKngBCOUe1ByN-Wg9g-Xv-PdGqTAAwyNSTY-IPJ-3TASVGDrUD4ITdO-73Cxqt9HHq-lW2L_tv5Ex7b-e98hAy3bL-Zv54Jf6_e0gx6pa9oaeAifsGDGEOKbEEd9MSBu-3tUerEhdnYtX5pzMl-JIV6jOeTfTgtWugBezj7wr7wKe8x6DfFxXn_6I-JV27G2LRNQC49Dh8Kblb-yWw5x3wnjUfx00JCdVN6TxCfT8UXr6kbHJ-UekG_29-UMGUuoKyT8BcfvzyHDPNKfdPoNGGkYpgva2_a9BQnNjHItYVTdOKXy0NEb2Gfx75vpf_lXy81z7bAB4110QhgpmmIMvL_G_YeKwPX6HYEL9AyQqbMjDqZTCTk). Let the streaming wars begin!
That's it for this week folks!
Cheers!
Kislay |