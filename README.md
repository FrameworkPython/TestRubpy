# TestRubpy

## تست متد create_channel_voice_chat
## نتیجه : Input Error
## کد استفاده شده:
```python
from rubpy import Client
import asyncio

async def main():
    async with Client(name='rubpy',display_welcome=False) as bot:
        result = await bot.create_channel_voice_chat("c0C92eN0c5755f5fda516d98cb13cd4a")
        print(result)

asyncio.run(main())
```
