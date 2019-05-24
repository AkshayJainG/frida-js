device = frida.get_remote_device()

pid = device.spawn(['com.snapchat.android'])

process = device.attach(pid

script = process.create_script(jscode)

script.on('message', on_message)

device.resume(pid)
