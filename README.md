# assignment2-Kalla
# Muralidhar Reddy Kalla
### My favorite place --- TajMahal,India.
The Taj Mahal is reminder of the Mughal era as it was built by **Mughal Emperor Shah Jahan** back in the **17th century**. A visit to the Taj Mahal takes me back in time to that magical era giving my mind a virtual break from the current times.

----

## Directions to TajMahal from Maryville
1. Go to kansas city Airport.
    1. Board Flight to Delhi,India.
    3. Board connecting flight to Agra Airport.
    6. Hire a taxi to TajMahal.
5. You can also go by bus from Agra Airport.
* A Good Camera
* Selfie Stick
* Food

[AbouMe.md Link](AboutMe.md)

---

## Popular Food/Drinks 
The table below illustrates about the best food/Drinks in various parts in the world and their price in dollars.

|Food/Drinks | Location  | Price($) |
|------------| --------- | ----- |
| Biryani    | Hyderabad | 10    |
| Momos      | Sikkim    | 15    |
| Bis Bele Bath|Karnataka | 7    |
|Dhokla      | Gujarath  | 5    |
| Mojito     | Cuba |     14    |

---

## Pithy Quotes
>Everything comes in time to him who knows how to wait.- *Leo Tolstoy* <br>
>Judge a man by his questions rather than by his answers.-*Voltaire*

---

## Bipartite graph
>A bipartite graph is a graph that does not contain any odd-length cycles. <https://en.wikipedia.org/wiki/Bipartite_graph>.

```
int n;
vector<vector<int>> adj;

vector<int> side(n, -1);
bool is_bipartite = true;
queue<int> q;
for (int st = 0; st < n; ++st) {
    if (side[st] == -1) {
        q.push(st);
        side[st] = 0;
        while (!q.empty()) {
            int v = q.front();
            q.pop();
            for (int u : adj[v]) { if (side[u] == -1) {
                    side[u] = side[v] ^ 1;
                    q.push(u);} else {
                    is_bipartite &= side[u] != side[v];
                } } } }
cout << (is_bipartite ? "YES" : "NO") << endl; 
```
<https://cp-algorithms.com/graph/bipartite-check.html>



