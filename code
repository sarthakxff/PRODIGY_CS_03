import re

def check_password_strength(password):
    # Criteria weights
    length_weight = 1
    uppercase_weight = 1
    lowercase_weight = 1
    digit_weight = 1
    special_char_weight = 2

    # Initialize score
    score = 0

    # Check length
    if len(password) >= 8:
        score += length_weight

    # Check uppercase letters
    if re.search(r"[A-Z]", password):
        score += uppercase_weight

    # Check lowercase letters
    if re.search(r"[a-z]", password):
        score += lowercase_weight

    # Check digits
    if re.search(r"\d", password):
        score += digit_weight

    # Check special characters
    if re.search(r"[!@#$%^&*(),.?\":{}|<>]", password):
        score += special_char_weight

    return score

def assess_strength(score):
    if score >= 9:
        return "Strong"
    elif score >= 6:
        return "Medium"
    else:
        return "Weak"

def main():
    password = input("Enter your password: ")
    strength_score = check_password_strength(password)
    strength_level = assess_strength(strength_score)
    print("Password strength:", strength_level)

if __name__ == "__main__":
    main()
