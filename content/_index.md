---
title: "Arkouda"
tagline: "Massive-scale data science,<br> from the comfort of your laptop"
codes:
  -
    name: "Arkouda"
    title: "Ready for supercomputers"
    code: |
      import arkouda as ak

      ak.startup('localhost', 5555)

      # Generate two large arrays
      a = ak.randint(0,2**32,2**38)        # ----> Won't fit on a single machine!
      b = ak.randint(0,2**32,2**38)        #       1TB of random integers.

      # add them
      c = a + b

      # Sort the array and print first 10 elements
      ak.sort(c)
      print(c[0:10])

  -
    name: "NumPy"
    title: "Industry standard"
    code: |
      import numpy as np



      # Generate two large arrays
      a = np.random.randint(0,2**32,2**28) # ----> smaller to fit on a single machine
      b = np.random.randint(0,2**32,2**28)

      # add them
      c = a + b

      # Sort the array and print first 10 elements
      np.ndarray.sort(c)
      print(c[0:10])

buttons:
    - name: "Try it Out"
      primary: true
      url: "https://github.com/bmcdonald3/chapelcon-2024-arkouda#readme"
    - name: "Tutorial Video"
      url: "https://www.youtube.com/watch?v=__pXYW359Ws"
    - name: "Chat on Gitter"
      icon: "message-square"
      url: "https://gitter.im/ArkoudaProject/community"

announcement:
    title: "Arkouda v2024.06.21 released!"
    content: |
      The new release includes improvements to the Array API implementation, which enables Arkouda arrays to provide distributed arrays for use in tools like XArray.

      [Read the release notes →](https://github.com/Bears-R-Us/arkouda/releases)
---

{{% section "arkouda-is" %}}
{{% section "quotes" %}}
{{% section "you-can" %}}
