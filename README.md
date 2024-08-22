# Quize
quiz_questions = [
    {
        "question": "What is the capital of France?",
        "options": ["A) Paris", "B) London", "C) Rome", "D) Berlin"],
        "answer": "A"
    },
    {
        "question": "Which planet is known as the Red Planet?",
        "options": ["A) Earth", "B) Mars", "C) Jupiter", "D) Venus"],
        "answer": "B"
    },
    {
        "question": "What is the largest ocean on Earth?",
        "options": ["A) Atlantic Ocean", "B) Indian Ocean", "C) Arctic Ocean", "D) Pacific Ocean"],
        "answer": "D"
    }
]

def run_quiz(questions):
    score = 0
    for q in questions:
        print(q["question"])  
        for option in q["options"]: 
            print(option)
        answer = input("Enter your answer (A, B, C, or D): ").upper()  # Get user input
        
        
        while answer not in ["A", "B", "C", "D"]:
            answer = input("Invalid input. Please enter A, B, C, or D: ").upper()

        if answer == q["answer"]:
            print("Correct!\n")
            score += 1
        else:
            print(f"Incorrect! The correct answer was {q['answer']}.\n")

    # Display final score
    print(f"Your final score is {score}/{len(questions)}")

# Run the quiz
if __name__ == "__main__":
    run_quiz(quiz_questions)
