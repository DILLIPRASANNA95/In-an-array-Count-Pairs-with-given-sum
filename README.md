# In-an-array-Count-Pairs-with-given-sum
def count_pairs_with_sum(arr, target_sum):
    count = 0
    num_dict = {}

    for num in arr:
        complement = target_sum - num

        if complement in num_dict:
            count += num_dict[complement]

        if num in num_dict:
            num_dict[num] += 1
        else:
            num_dict[num] = 1

    return count

arr = [1, 5, 7, -1, 5]
target_sum = 6

pair_count = count_pairs_with_sum(arr, target_sum)
print(f"Number of pairs with sum {target_sum}: {pair_count}")
