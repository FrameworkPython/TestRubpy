### متد:
`create_channel_voice_chat`

### شرح مشکل:
`ارور Input به کاربر نمایش داده میشود، این متد فقط یک پارامتر چنل گویید میخواهد اما حتی با این پارامتر، ارور میدهد`
### کد استفاده شده:
```python
from rubpy import Client
import asyncio

async def main():
    async with Client(name='rubpy', display_welcome=False) as bot:
        result = await bot.create_channel_voice_chat("c0C92eN0c5755f5fda516d98cb13cd4a")
        print(result)

asyncio.run(main())
```
### ارور دریافتی:
```plaintext
Traceback (most recent call last):
  File "/data/user/0/ru.iiec.pydroid3/files/accomp_files/iiec_run/iiec_run.py", line 31, in <module>
    start(fakepyfile,mainpyfile)
  File "/data/user/0/ru.iiec.pydroid3/files/accomp_files/iiec_run/iiec_run.py", line 30, in start
    exec(open(mainpyfile).read(),  __main__.__dict__)
  File "<string>", line 9, in <module>
  File "/data/user/0/ru.iiec.pydroid3/files/aarch64-linux-android/lib/python3.11/asyncio/runners.py", line 190, in run
    return runner.run(main)
           ^^^^^^^^^^^^^^^^
  File "/data/user/0/ru.iiec.pydroid3/files/aarch64-linux-android/lib/python3.11/asyncio/runners.py", line 118, in run
    return self._loop.run_until_complete(task)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/data/user/0/ru.iiec.pydroid3/files/aarch64-linux-android/lib/python3.11/asyncio/base_events.py", line 653, in run_until_complete
    return future.result()
           ^^^^^^^^^^^^^^^
  File "<string>", line 6, in main
  File "/data/user/0/ru.iiec.pydroid3/files/aarch64-linux-android/lib/python3.11/site-packages/rubpy/methods/channels/create_channel_voice_chat.py", line 18, in create_channel_voice_chat
    return await self.builder('createChannelVoiceChat', input={'channel_guid': channel_guid})
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/data/user/0/ru.iiec.pydroid3/files/aarch64-linux-android/lib/python3.11/site-packages/rubpy/methods/advanced/build.py", line 62, in builder
    raise exceptions(status_det)(result, request=None)
rubpy.exceptions.InvalidInput: {'status': 'ERROR_GENERIC', 'status_det': 'INVALID_INPUT'}

[Program finished]
```
