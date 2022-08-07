# leetcode-3-longest...


1)  

        def isUnique(ls):
                array = []
                for i in range(len(ls)):
                        if ls[i] in array:
                                return False
                        array+=ls[i]
                return True

        def lengthOfLongestSubstring(s):
                ls = list(s)
                sub1= []
                sub2 = []
                longestLen = len(ls[0])
                for i in range(0,len(ls)-1):
                        sub1 += s[i]
                        if isUnique(sub1) is True and len(sub1) > longestLen:
                                longestLen = len(sub1)
                        for j in range(i+1,len(ls)):
                                sub2 += [s[j]]
                                if isUnique(sub2) is True and len(sub2) > longestLen:
                                        longestLen = len(sub2)
                        sub2.clear()              
        s = "pwwkew"
        print(lengthOfLongestSubstring(s))
        
2)
