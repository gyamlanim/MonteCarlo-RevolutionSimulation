# MonteCarlo-RevolutionSimulation

This project is based on Timur Kuran’s paper “Now Out of Never: The Element of Surprise in the East European Revolution of 1989”, which explains how revolutions happen. Kuran argues that people often hide their true opinions due to fear or social pressure, but when enough individuals start openly expressing their views, others may feel encouraged to join in, eventually leading to a revolution. This project simulates how a group of individuals (represented by a list of random values) might decide to join a revolution as more people gain enough courage to rebel.

**Simulation Overview**:
- **Population (A)**: This is a group of people, each represented by a random number between 0 and 100. The lower a person's number, the more likely they are to revolt.
- **Revolutionary Threshold (S)**: This is a number that represents how "safe" it feels for people to rebel. Initially, it's randomly chosen, but it changes as more people revolt.
- **Revolters**: These are the people whose number (willingness to revolt) is lower than the current revolutionary threshold (S). As more people revolt, the threshold changes, making it easier for others to join.

**How It Works**:
1. **Initial Setup**: We start with a group of people (A) with random willingness to revolt and an initial threshold (S), which indicates how risky or safe it feels to revolt.
2. **Revolution Process**: The program checks who in the group is willing to revolt based on the current threshold. If a person’s number is less than or equal to the threshold, they join the revolters.
3. **Threshold Update**: Each time more people join the revolt, the threshold (S) is updated. The more people revolt, the safer it feels for others to join.
4. **Revolter Adjustments**: Sometimes, as the threshold changes, a few revolters might stop revolting if the new threshold makes it unsafe for them.
5. **End of the Process**: The revolution continues until no more people are willing to join, meaning the revolutionary movement has stabilized (revolution stops growing).


