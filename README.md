# COMP3005A Final Project
# Zeming Lin (solo): GROUP 100
# 101302626
# DB: Health and Fitness Club Management System

# Entities (7): 
# 1.	Members
# 2.	Trainers
# 3.	Administrative Staff
# 4.	Individual Training Sessions
# 5.	Group Fitness Classes
# 6.	Rooms
# 7.    Room Booking
# 
# Relationships (8):
# 1.	Trainer trains members
# 2.	Member books a group session
# 3.	Member books a personal session
# 4.    Trainers work with administrative staff.
# 5.	Staff reserves a room.
# 6.	Staff defines group fitness classes.
# 7.	Staff registers/updates members.
# 8.    Room has different bookings

# Roles (3):
# 1.	Member
# 2.	Trainer
# 3.	Staff

# Operations (8):
# Members
#    1.	User registration 
#    2.	Log health metrics
#    3.	PT Session Booking
#    4.	Group Fitness Class Registration

# Trainers
#    5. Set Availability
#    6. Schedule View

# Administrative Staff
#    7. Room booking (for personal traing sessions)
#    8. Class Definition


# Assumptions:
# Each trainer has a unique trainer ID
# Each administrative staff member has a unique employee ID
# Each member has at most 1 personal trainer

Trigger: check overlapping booking/room capacity/trainer availability


# Index: Trainer Availabilities Date and Start_time
# Availabilities(trainer_id, date_of_record, start_time);

# VIEW: Member_info--Most recent health metrics, fitness goals, upcoming individual training session and group fitness classes of Members
# Member_Dashboard is a filtered Member_info
# -- need to provide trainer_id and Member to have the rows of all the upcoming classes of a member-trainer pair
# -- need to order by date_of_record and start_time to find the row with the soonest upcoming group fitness class with the same trainer


# Trigger: update Availabilites after an insertion to Individual_Training_Sessions
# Trigger: update Availabilites after an insertion to Group_Fitness_Classes
# Youtube Video Link: https://youtu.be/G7ak72xrfGA
# Github Link: https://github.com/ZEMLIN26/COMP3005A_FINAL_PROJECT.git

