body {
  font-family: Arial, sans-serif;
  background-color: #fdfdfd;
  margin: 0;
  padding: 0;
}

header {
  background-color: #2e8b57;
  color: white;
  padding: 20px;
  text-align: center;
}

nav a {
  color: white;
  margin: 0 10px;
  text-decoration: none;
  font-weight: bold;
}

main {
  padding: 20px;
}

#produtos {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
}

.produto {
  border: 1px solid #ccc;
  padding: 10px;
  width: 200px;
  border-radius: 10px;
  background: #fff;
  text-align: center;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}

.produto img {
  width: 100%;
  border-radius: 8px;
}

.produto h2 {
  font-size: 18px;
  margin: 10px 0 5px;
}

.produto p {
  font-size: 14px;
  margin: 5px 0;
}

.produto .preco {
  font-weight: bold;
  color: #2e8b57;
  margin: 8px 0;
}

button {
  background-color: #2e8b57;
  color: white;
  border: none;
  padding: 10px;
  margin-top: 10px;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #276f48;
}

#carrinho {
  margin-top: 40px;
}
