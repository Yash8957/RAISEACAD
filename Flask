# app.py - The Enchanted Backend

from flask import Flask, jsonify, request

app = Flask(__name__)

# Sample course data (because even wizards need to learn)
courses = [
    {
        "id": 1,
        "title": "Potion Brewing 101",
        "instructor": "Professor Salamander",
        "duration": "6 weeks",
    },
    {
        "id": 2,
        "title": "Quantum Spellcasting",
        "instructor": "Archmage Aurora",
        "duration": "8 weeks",
    },
    {
        "id": 3,
        "title": "Dragonology",
        "instructor": "Dr. Ignis",
        "duration": "10 weeks",
    },
]

# Enchant the /courses endpoint
@app.route("/courses", methods=["GET"])
def get_courses():
    """
    Retrieve a list of available courses.
    """
    return jsonify(courses)

# Enchant the /enroll endpoint
@app.route("/enroll", methods=["POST"])
def enroll_student():
    """
    Enroll a student in a course.
    """
    data = request.get_json()
    student_name = data.get("name")
    course_id = data.get("course_id")

    # Inscribe the student's name in the ancient Book of Enrollments
    # (In reality, just print a message)
    print(f"📜 {student_name} has enrolled in Course ID {course_id}!")

    return jsonify({"message": "Enrollment successful!"})

if __name__ == "__main__":
    print("🌟 RAISEACAD Backend is casting spells! 🌟")
    app.run(debug=True)
