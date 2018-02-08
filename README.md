# 10954---Add-All

#include <iostream>

#include <algorithm>

#include <queue>

#include <vector>

#include <functional>

using namespace std;

int main()
{

	int res = 0, num;

	while (cin >> num && num)
	{
		res = 0;

		priority_queue<int, vector<int>, greater<int> >q;
		for (int i = 0, x; i<num; i++)
		{
			cin >> x;
			q.push(x);
		}

		while (q.size() > 1)
		{
			int a, b;
			a = q.top(), q.pop();

			b = q.top(), q.pop();

			q.push(a + b);
			res += (a + b);
		}
		cout << res << endl;
	}
	return 0;
}
