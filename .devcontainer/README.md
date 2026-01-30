foco

```javascript
async function getOllamaResponse() {
    try {
        const response = await fetch('http://127.0.0.1:11434/api/generate', {
            method: 'POST',
            headers: { 'Content-Type': 'application/json' },
            body: JSON.stringify({
                model: 'openhermes',
                prompt: 'Why is the sky blue?',
                stream: false // Crucial for a single response
            })
        });

        if (!response.ok) {
            throw new Error(`HTTP error! status: ${response.status}`);
        }

        const data = await response.json();
        console.log('Full Response Object:', data);
        console.log('The answer is:', data.response);
    } catch (error) {
        console.error('Error fetching from Ollama:', error);
    }
}

// Call the function
getOllamaResponse();
```
