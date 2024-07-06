To build acustom form controls
css code:



body { 

  font-family: "Roboto", sans-serif; 
} 

  
.select-container { 

  display: flex; 

  flex-direction: column; 

  width: 400px; 
} 

  
.select-container .option-container { 

  background: #2f3640; 

  color: #f5f6fa; 

  max-height: 0; 

  width: 100%; 

  opacity: 0; 

  transition: all 0.4s; 

  border-radius: 8px; 

  overflow: hidden; 

  order: 1; 
} 

  
.selected { 

  background: #2f3640; 

  border-radius: 8px; 

  margin-bottom: 8px; 

  color: #f5f6fa; 

  position: relative; 

  order: 0; 
} 

  
.selected::after { 

  content: "v"; 

  position: absolute; 

  height: 100%; 

  width: 30px; 

  right: 10px; 

  top: 11px; 

  transition: all 0.4s; 
} 

  
.select-container .option-container.active { 

  max-height: 240px; 

  opacity: 1; 

  overflow-y: scroll; 
} 

  
.select-container .option-container.active + .selected::after { 

  transform: rotateX(180deg); 

  top: -14px; 
} 

  
.select-container .option-container::-webkit-scrollbar { 

  width: 8px; 

  background: #0d141f; 

  border-radius: 0 8px 8px 0; 
} 

  
.select-container .option-container::-webkit-scrollbar-thumb { 

  background: #525861; 

  border-radius: 0 8px 8px 0; 
} 

  
.select-container .option, 
.selected { 

  padding: 12px 24px; 

  cursor: pointer; 
} 

  
.select-container .option:hover { 

  background: #414b57; 
}

