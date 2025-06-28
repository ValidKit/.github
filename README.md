# ValidKit

**Email validation infrastructure built for AI agents and high-scale automation.**

## 🚀 Why ValidKit?

AI agents need reliable email validation at scale. ValidKit provides:

- **10,000 emails in 7-10 seconds** - Built for agent-scale operations
- **80% smaller responses** - Token-optimized for LLM efficiency  
- **3,000 validations/second** - No more rate limit frustrations
- **Agent-first design** - No dashboards, just APIs

## 📦 Quick Start

### Node.js/TypeScript
```bash
npm install @validkit/sdk
```

```typescript
import { ValidKit } from '@validkit/sdk';

const validkit = new ValidKit({ api_key: 'your-api-key' });
const result = await validkit.verifyEmail('user@example.com');
```

### Python
```bash
pip install validkit
```

```python
from validkit import ValidKit

async with ValidKit(api_key='your-api-key') as validkit:
    result = await validkit.verify_email('user@example.com')
```

### Command Line
```bash
npm install -g @validkit/cli
validkit verify user@example.com
```

## 🛠️ Available SDKs

| Repository | Package | Description |
|------------|---------|-------------|
| [validkit-typescript-sdk](https://github.com/ValidKit/validkit-typescript-sdk) | `@validkit/sdk` | TypeScript/JavaScript SDK with full type support |
| [validkit-python-sdk](https://github.com/ValidKit/validkit-python-sdk) | `validkit` | Async Python SDK built on asyncio |
| [validkit-cli](https://github.com/ValidKit/validkit-cli) | `@validkit/cli` | Command-line interface for scripts and automation |

## 🎯 Built for AI Agents

### LangChain Integration
```python
from langchain.tools import Tool
from validkit import ValidKit

validkit_tool = Tool(
    name="Email Validator",
    func=lambda email: validkit.verify_email(email),
    description="Validates email addresses"
)
```

### Token-Optimized Responses
```javascript
// 80% smaller responses with compact format
const results = await validkit.verifyBatch(emails, {
  format: ResponseFormat.COMPACT
});
// Returns: [{e: "user@example.com", v: true}, ...]
```

### Multi-Agent Tracing
```typescript
// Track validation across agent workflows
const result = await validkit.verifyEmail(email, {
  trace_id: 'agent-123',
  parent_id: 'workflow-456'
});
```

## 📊 Features

- ✅ **Real-time validation** - Instant email verification
- ✅ **Bulk processing** - Up to 10,000 emails per request
- ✅ **Smart retries** - Automatic retry with exponential backoff
- ✅ **Async operations** - Non-blocking for large batches
- ✅ **Agent Signal Pool** - Collaborative validation data
- ✅ **99.9% uptime SLA** - Enterprise reliability

## 🔗 Resources

- [Documentation](https://docs.validkit.com)
- [API Reference](https://docs.validkit.com/api)
- [Status Page](https://status.validkit.com)
- [Pricing](https://validkit.com/pricing)

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) in each repository.

## 📝 License

All ValidKit SDKs are released under the MIT License.

---

**Ready to validate emails at agent scale?** [Get your API key →](https://validkit.com)
