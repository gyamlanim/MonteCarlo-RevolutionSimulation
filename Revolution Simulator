import random

# Initialize population (A) and revolutionary threshold (S)
# A represents a population of 10 individuals with random thresholds between 0 and 100.
A = [random.randint(0, 100) for _ in range(10)]

# S is the initial revolutionary threshold, which represents how "safe" it feels to revolt.
'''There’s a choice to make between 0 and a random number for S.
It should be 0 according to the paper, but for testing the overall functionality of the code we need a larger number so the revolution actually happens.
It also seems unlikely that everyone will agree exactly with the government.'''
S = random.randint(0, 100)

# Display the initial state of the population and the initial revolutionary threshold.
print("Initial state of A:", A)
print("Initial threshold S:", S)

# Initialize an empty list to keep track of who is revolting.
revolters = []

# Main revolution loop
while True:
    # Create a list to track new revolters in the current iteration.
    new_revolters = []

    # Find individuals willing to revolt (those whose threshold is less than or equal to S).
    for a in A:
        if a <= S and a not in revolters:
            new_revolters.append(a)

    # If no new revolters are found, exit the loop.
    if not new_revolters:
        break

    # Add new revolters to the main revolters list.
    # We use extend to add multiple elements to the list.
    revolters.extend(new_revolters)

    # Update the revolutionary threshold S.
    # S is now based on the proportion of revolters in the population.
    S = (len(revolters) / len(A)) * 100

    # Update the revolters list to remove anyone whose threshold is now above S.
    remaining_revolters = []
    for r in revolters:
        if r <= S:
            remaining_revolters.append(r)
    revolters = remaining_revolters

    # Print the current state of revolters and the updated threshold S.
    print("Revolters:", revolters)
    print("Updated threshold S:", S)

# Final results
print("Final state of A:", A)
print("Final threshold S:", S)
print("Final number of revolters:", len(revolters))
