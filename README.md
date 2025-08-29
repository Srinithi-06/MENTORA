# MENTORA
**Description:**
A Java-based application that helps students track study habits, skill development, and learning goals.
Users can log study/skill sessions, monitor progress, and stay motivated with insights & motivational quotes.

**Problem Statement:**
Many students struggle to track their study time, skill development, and consistency. 
Without proper tracking, they lose motivation and fail to achieve learning milestones🚹.

**Target Users:**
College students
Self-learners
Professionals developing new skills 

**OOP Concepts in Mentora**
*Encapsulation ==> Where we use it: In classes like User, Session, and Goal, we keep variables private:
Purpose:
Protects data from direct modification.
Example: A user cannot directly set hours = -5. Instead, they must call setHours(), where we can validate input.
This ensures data security and correctness in Mentora.

*Inheritance ==> Where we use it: StudySession and SkillSession both inherit from the base Session class.
Purpose:
Avoids code duplication → common fields like sessionId, date, and hours are in Session.
Specific behavior is added in child classes → StudySession may track subject, while SkillSession may track skill type.
Makes Mentora scalable if later we add more session types (like "WorkoutSession").

*Polymorphism==>Where we use it: Both StudySession and SkillSession override the method getSummary().
Purpose:
The same method name behaves differently based on object type.
Provides flexibility → Mentora can treat all sessions as Session but still display custom summaries.

*Abstraction==>Where we use it: The Session class can be abstract since we never create a raw "Session", only specific ones like StudySession or SkillSession.
Purpose:
Hides unnecessary details and forces child classes to implement important methods.
Makes Mentora’s design clean and enforceable — every type of session must define how its summary is shown.


