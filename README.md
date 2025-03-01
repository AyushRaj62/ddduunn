#include <bits/stdc++.h>
using namespace std;

int dx[4] = {-1, 1, -1, 1}, dy[4] = {-1, -1, 1, 1};

int main()
{
    int t;
    cin >> t;
    while (t--)
    {
        long long a, b;
        cin >> a >> b;
        
        long long x_king, y_king;
        cin >> x_king >> y_king;
        
        long long x_queen, y_queen;
        cin >> x_queen >> y_queen;
 
        set<pair<int,int>> king_hits, queen_hits;

        for(int j = 0; j < 4; j++){ // 4
            king_hits.insert({x_king + dx[j]*a, y_king + dy[j]*b});  
            king_hits.insert({x_king + dx[j]*b, y_king + dy[j]*a});

            queen_hits.insert({x_queen + dx[j]*a, y_queen + dy[j]*b});
            queen_hits.insert({x_queen + dx[j]*b, y_queen + dy[j]*a});
        }

        int ans = 0; 
        
        for(auto pos : king_hits)  
            if(queen_hits.find(pos) != queen_hits.end()) 
                ans++;
            
            // if (queen.count(pos)) ans++;
        
        cout << ans << endl;
    }
    return 0;
}

// tc - O(8*log2(8)) = O(8*3) = O(24)
// sc - O(8)





#include <bits/stdc++.h>
using namespace std;
#define int long long

void solve() {
    
}

signed main() {
    ios_base::sync_with_stdio(0);
    cin.tie(0); cout.tie(0);
    int t;
    cin >> t;

    while (t--) {
        solve();
    }
}
