# graoh_bfs
void bfs(int n,vector<vector<int>>& edges, int s, vector<bool>&vis ){
         queue<int>q;
         vis[s]=true;
         q.push(s);
         while(!q.empty()){
            
            int x=q.front();
            q.pop();

            for(auto neigh: edges[x]){
                if(vis[neigh]==false){
                    vis[neigh]=true;
                    q.push(neigh);
                }
            }
         }
    }
