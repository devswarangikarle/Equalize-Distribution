# Equalize-Distribution

In a small town, three friends - Riya, Sam, and Vikram - each have some magical stones. Riya has A stones, Sam has B stones, and Vikram has C stones. You, as their friend, have N extra magical stones that you want to distribute among them. Your goal is to distribute all N stones such that Riya, Sam, and Vikram each end up with the same number of stones in the end.
Can you figure out how to distribute the stones equally among them?

def can_distribute_equally(A, B, C, N):
    max_stones = max(A, B, C)
    total_needed = (max_stones - A) + (max_stones - B) + (max_stones - C)
    
    remaining_stones = N - total_needed
    
    if remaining_stones >= 0 and remaining_stones % 3 == 0:
        return "YES"
    else:
        return "NO"

A, B, C, N = map(int, input().split())
print(can_distribute_equally(A, B, C, N))
