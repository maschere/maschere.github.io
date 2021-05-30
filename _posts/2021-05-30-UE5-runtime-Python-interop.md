## Unreal Engine 5 runtime interop with Python in real-time using TCP sockets

<video width="600" height="400" controls autoplay muted loop>
  <source type="video/mp4" src="/videos/ue5-python-interop.mp4">
</video>

---

For several planned projects I need reasonably fast, but flexible (cross-platform) two-way communication between [UE5](https://www.unrealengine.com/en-US/blog/unreal-engine-5-is-now-available-in-early-access) (should work the same for UE 4.26) and an external Python process. Though named-pipes or shared memory might produce a little less overhead, I opted for TCP sockets for their ease of use, platform-independence and flexibility. Particularly if remote communication becomes a requirement down the line.

The video above shows a rudimentary proof-of-concept I got running this afternoon. It uses Unreal's C++ [FSocket](https://docs.unrealengine.com/5.0/en-US/API/Runtime/Sockets/FSocket/) class and Python's socket / [socketserver](https://docs.python.org/3/library/socketserver.html).

Next, I will extend and clean up the code to make the whole thing easy to (re-)use. Maybe I'll look into compiling into a UE5 plugin. The code will be open-sourced on my Github in any case.