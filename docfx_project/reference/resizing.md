[!include[links](../linksinc.md)]

# Resizing Frames
There are two ways frames may be resized, by the GPU or by the CPU.

The CPU methods are simple to use, and are based around NV12 frame resizing.


We recommend starting with the simple CPUs methods, and switching to GPU methods as your project gets mature and need optimization. 




### CPU based resizing method

### GPU based resizing method

The GPU resizing methods can be used by using the these classes: [StreamDecoder],[StreamTranscoder]
The trick is to properly configure the inputs to the constructors.
The encoder does not do resizing at the time.


To get GPU resizing to occur in the [StreamDecoder], the constructor containing two [mfxVideoParam]s must be used.  The second [mfxVideoParam] named: mfxVPPParams controls resizing.

You can use the 

To get GPU resizing to occur in the StreamTranscoder, the TranscoderConfig must have the [mfxVideoParam] element,  [vppParams] setup properly.




