<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Spanning Tree Game</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; }
        canvas { background-color: #f8f9fa; border: 1px solid black; }
        .message { margin-top: 10px; font-weight: bold; color: red; }
    </style>
</head>
<body>
    <h1>Costruisci uno Spanning Tree</h1>
    <p>Clicca sugli archi per selezionarli e costruire uno spanning tree minimo.</p>
    <canvas id="graphCanvas" width="500" height="500"></canvas>
    <p class="message" id="message"></p>
    <script>
        const canvas = document.getElementById("graphCanvas");
        const ctx = canvas.getContext("2d");
        const message = document.getElementById("message");
        
        let nodes = [
            {x: 100, y: 100}, {x: 400, y: 100}, {x: 250, y: 200},
            {x: 100, y: 400}, {x: 400, y: 400}
        ];
        
        let edges = [
            {a: 0, b: 1, weight: 2}, {a: 0, b: 2, weight: 3}, {a: 1, b: 2, weight: 1},
            {a: 2, b: 3, weight: 4}, {a: 2, b: 4, weight: 5}, {a: 3, b: 4, weight: 6}
        ];
        
        let selectedEdges = [];
        
        function drawGraph() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            edges.forEach(edge => {
                const {x: x1, y: y1} = nodes[edge.a];
                const {x: x2, y: y2} = nodes[edge.b];
                ctx.strokeStyle = selectedEdges.includes(edge) ? "green" : "black";
                ctx.lineWidth = selectedEdges.includes(edge) ? 3 : 1;
                ctx.beginPath();
                ctx.moveTo(x1, y1);
                ctx.lineTo(x2, y2);
                ctx.stroke();
                ctx.fillStyle = "black";
                ctx.fillText(edge.weight, (x1 + x2) / 2, (y1 + y2) / 2);
            });
            
            nodes.forEach(node => {
                ctx.fillStyle = "blue";
                ctx.beginPath();
                ctx.arc(node.x, node.y, 10, 0, Math.PI * 2);
                ctx.fill();
            });
        }
        
        function find(parent, i) {
            if (parent[i] === i) return i;
            return find(parent, parent[i]);
        }
        
        function union(parent, rank, x, y) {
            let rootX = find(parent, x);
            let rootY = find(parent, y);
            if (rootX !== rootY) {
                if (rank[rootX] < rank[rootY]) parent[rootX] = rootY;
                else if (rank[rootX] > rank[rootY]) parent[rootY] = rootX;
                else { parent[rootY] = rootX; rank[rootX]++; }
            }
        }
        
        function checkCycle() {
            let parent = [], rank = [];
            for (let i = 0; i < nodes.length; i++) {
                parent[i] = i;
                rank[i] = 0;
            }
            for (let edge of selectedEdges) {
                let x = find(parent, edge.a);
                let y = find(parent, edge.b);
                if (x === y) return true;
                union(parent, rank, x, y);
            }
            return false;
        }
        
        function checkWin() {
            if (selectedEdges.length === nodes.length - 1) {
                message.textContent = "Complimenti! Hai completato lo Spanning Tree!";
                return true;
            }
            return false;
        }
        
        canvas.addEventListener("click", (event) => {
            const rect = canvas.getBoundingClientRect();
            const clickX = event.clientX - rect.left;
            const clickY = event.clientY - rect.top;
            
            for (let edge of edges) {
                const {x: x1, y: y1} = nodes[edge.a];
                const {x: x2, y: y2} = nodes[edge.b];
                let distance = Math.abs((y2 - y1) * clickX - (x2 - x1) * clickY + x2 * y1 - y2 * x1) /
                               Math.sqrt((y2 - y1) ** 2 + (x2 - x1) ** 2);
                if (distance < 10) {
                    if (selectedEdges.includes(edge)) {
                        selectedEdges = selectedEdges.filter(e => e !== edge);
                    } else {
                        selectedEdges.push(edge);
                        if (checkCycle()) {
                            message.textContent = "Errore: hai formato un ciclo!";
                            selectedEdges.pop();
                        } else {
                            message.textContent = "";
                            checkWin();
                        }
                    }
                    drawGraph();
                    break;
                }
            }
        });
        
        drawGraph();
    </script>
</body>
</html>
