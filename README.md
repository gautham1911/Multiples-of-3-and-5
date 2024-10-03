# Multiples-of-3-and-5
This problem is a programming version of Problem 1 from projecteuler.net

If we list all the natural numbers below 10  that are multiples of 3  or 5, we get 3,5,6 and9 . The sum of these multiples is 23.

Find the sum of all the multiples of 3 or5  below N.

#include <map>
#include <set>
#include <list>
#include <cmath>
#include <ctime>
#include <deque>
#include <queue>
#include <stack>
#include <string>
#include <bitset>
#include <cstdio>
#include <limits>
#include <vector>
#include <climits>
#include <cstring>
#include <cstdlib>
#include <fstream>
#include <numeric>
#include <sstream>
#include <iostream>
#include <algorithm>
#include <unordered_map>

using namespace std;


int main(){
    int t;
    cin >> t;
       
    while(t--)
    {
        int n;
        cin >> n;               
       
        unsigned long long sum3, sum5, sum15;
        unsigned long long num3 = 3, num5 = 5, num15 = 15, i;
        
        unsigned long long vals[3] = {3, 5, 15};
        
        for(int i=0; i<3; i++)
        {
            long long x = (n-1)/vals[i];
            vals[i] = ((vals[i]*x*(x+1))/2);            
        }
        cout<<(vals[0]+vals[1]-vals[2])<<endl;
    }
    return 0;
}

