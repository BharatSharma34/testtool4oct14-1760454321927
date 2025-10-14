# TestTool4oct14

test

## 🚀 Quick Start

### Edit Your Code
1. Open `tool.py`
2. Modify the `main(event_body)` function
3. Add any helper functions you need

### Deploy
1. Commit and push to the `main` branch
2. GitHub Actions will automatically:
   - Merge your code with the Lambda handler
   - Install dependencies from `requirements.txt`
   - Deploy to AWS Lambda

### Add Dependencies
Add Python packages to `requirements.txt`:
```
requests>=2.28.0
pandas>=1.5.0
```

## ⚠️ Important Notes

- **DO NOT** modify the Lambda handler code
- **DO NOT** add `lambda_handler` function to `tool.py`
- The handler is automatically appended during deployment
- Only edit the `main()` function and helper functions in `tool.py`

## 📝 Example

```python
def main(event_body):
    user_input = event_body.get('message', 'Hello')
    return {
        "success": True,
        "result": f"Processed: {user_input}"
    }
```

## 🔧 Testing Locally

```python
# Test your main function
result = main({"message": "test"})
print(result)
```
