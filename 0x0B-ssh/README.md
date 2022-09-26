class Solution:
    def dailyTemperatures(self, temperatures: List[int]) -> List[int]:
        ans = [0] * len(temperatures)
        stack = []
        for idx, val in enumerate(temperatures):
            while stack and val > stack[-1][-1]:
                index, t = stack.pop()
                ans[index] = idx - index
            stack.append([idx, val])
        return ans