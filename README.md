# Belajar OpenCV on Rust ([Face Detection](https://github.com/twistedfall/opencv-rust/blob/master/examples/video_facedetect.rs))

Steps to reproduce on Linux - [OpenCV: Installation in Linux](https://docs.opencv.org/master/d7/d9f/tutorial_linux_install.html) with some adjustment:
1. Install dependencies (cmake, g++/gcc, wget, unzip)
2. Install OpenCV (3.2, 3.4, 4.x)
  1. Manual
    1. Download from OpenCV Repo - Latest 4.5.3 (```wget -O opencv.zip https://github.com/opencv/opencv/archive/master.zip```)
    2. Unpack downloaded OpenCV (```unzip opencv.zip```)
    3. Create build directory (```mv opencv-master opencv && mkdir -p build && cd build```)
    4. Pre-Configure (```rm ../opencv/CMakeCache.txt```)
    5. Configure with libgtk2.0 disable qt (```cmake -D WITH_QT=OFF ../opencv```)
    6. Build (```make```), you can run compilation processes in parallel by using (```make -j4```)
    7. Run installation, you need elevated privileges (```sudo make install```)
    8. Post-Configure (```export OpenCV_DIR=<*.cmake location> && export LD_LIBRARY_PATH=<*.so location>```)
  2. [Prebuilt version](https://docs.opencv.org/master/d0/d3d/tutorial_general_install.html#tutorial_general_install_prebuilt)
3. Run Apps (```cargo run```)
