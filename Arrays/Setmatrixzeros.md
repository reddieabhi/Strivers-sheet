

class Solution:
    def setZeroes(self, matrix: List[List[int]]) -> None:
        """
        Do not return anything, modify matrix in-place instead.
        """
        i_dict = {}
        j_dict = {}
        for i in range(len(matrix)):
            for j in range(len(matrix[0])):
                if matrix[i][j] == 0:
                    i_dict[i] = 1
                    j_dict[j] = 1
        for i in range(len(matrix)):
            for j in range(len(matrix[0])):
                if i in i_dict or j in j_dict:
                    matrix[i][j] = 0
        
        
