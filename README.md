# 🎨 Color Transfer by Lucas

A custom ComfyUI node that transfers the color palette from a reference image to a content image using advanced L*a*b* color space statistics.

## ✨ Features

This node allows you to:

- 🎨 **Transfer Color Palettes**: Apply the color scheme from one image to another
- 💪 **Adjustable Transfer Strength**: Control how much of the reference colors are applied (0.0 to 1.0)
- 🔬 **L*a*b* Color Space**: Uses perceptually uniform color space for better results
- 📊 **Statistical Approach**: Matches mean and standard deviation of color channels
- 🎯 **Preset Options**: Quick access to subtle and strong transfer presets

## 📦 Installation

### Method 1: Manual Installation

1. Download the `color_transfer_by_lucas.zip` file
2. Extract its contents into your ComfyUI's `custom_nodes` folder:
   ```
   ComfyUI/custom_nodes/color_transfer_by_lucas/
   ```
3. Restart ComfyUI

### Method 2: Via ComfyUI Manager (if available)

1. Open ComfyUI Manager
2. Search for "Color Transfer by Lucas"
3. Click "Install"
4. Restart ComfyUI

## 🚀 How to Use

1. In ComfyUI, search for "Color Transfer by Lucas" in the `image/color` category
2. Add the node to your workflow
3. Connect your images:
   - **image_content**: The image you want to change the colors of
   - **image_reference**: The image whose color palette you want to copy
4. Adjust the **Transfer Strength** slider:
   - `0.0` = No transfer (original image unchanged)
   - `1.0` = Full transfer (complete color replacement)
   - `0.3-0.5` = Subtle color adjustment
   - `0.7-0.9` = Strong color change
5. The result will be available at the output

## 🎯 Usage Examples

### Portrait Color Grading
- **Content**: Portrait photo
- **Reference**: Professional headshot with desired color grading
- **Strength**: 0.4-0.6 for natural results

### Landscape Mood Transfer
- **Content**: Landscape photo
- **Reference**: Image with desired atmospheric mood
- **Strength**: 0.5-0.8 for dramatic effect

### Artistic Style Transfer
- **Content**: Regular photo
- **Reference**: Painting or artwork
- **Strength**: 0.6-1.0 for artistic effect

## 🎨 Interface Features

- **Colorful Gradient Slider**: Visual representation of color transfer strength
- **Preset Options**: Right-click menu with quick presets:
  - 🎯 Subtle Transfer (0.3)
  - 🌟 Strong Transfer (0.8)
  - 🔄 Reset to Full Transfer (1.0)
- **Information Dialog**: Detailed explanation of the algorithm
- **Custom Styling**: Purple gradient theme with enhanced visual appeal

## 🔬 Technical Details

### Algorithm
The node uses statistical color transfer in the L*a*b* color space:

1. **Convert to L*a*b***: Both images are converted to perceptually uniform L*a*b* color space
2. **Calculate Statistics**: Mean and standard deviation are computed for each channel (L, a, b)
3. **Apply Transfer**: Content image statistics are adjusted to match reference image
4. **Blend Results**: Final result is blended with original based on transfer strength
5. **Convert Back**: Result is converted back to RGB color space

### Benefits of L*a*b* Color Space
- **Perceptually Uniform**: Changes correspond better to human vision
- **Separates Luminance**: L channel handles brightness, a/b handle color
- **Better Color Matching**: More natural color transfer results

## 📋 Requirements

- ComfyUI
- Python 3.8+
- PyTorch 2.0+
- OpenCV (cv2)
- NumPy
- PIL (Pillow)

## 🐛 Troubleshooting

### Node doesn't appear in the list
- Verify the folder was extracted correctly into `custom_nodes`
- Restart ComfyUI completely
- Check the console for error messages

### Error "module 'cv2' has no attribute..."
- Install OpenCV: `python -m pip install opencv-python`
- Use the specific Python environment of ComfyUI for installation

### Poor color transfer results
- Try different transfer strength values
- Ensure reference and content images have similar lighting
- Use images with compatible content types
- Consider the mood and style of both images

### Performance issues
- Large images may take longer to process
- Consider resizing images before color transfer for faster results
- The algorithm is optimized but complex calculations take time

## 💡 Tips for Best Results

### Image Selection
- **Similar Content**: Works best with images of similar subject matter
- **Good Lighting**: Both images should have clear, well-lit subjects
- **Color Variety**: Reference images with rich color palettes work better

### Transfer Strength Guidelines
- **0.1-0.3**: Very subtle color adjustment
- **0.3-0.5**: Natural color grading
- **0.5-0.7**: Noticeable color change
- **0.7-0.9**: Strong artistic effect
- **0.9-1.0**: Complete color replacement

### Workflow Tips
- Experiment with different reference images
- Try multiple transfer strengths to find the sweet spot
- Combine with other color correction nodes for fine-tuning
- Save successful combinations as presets in your workflow

## 📝 Changelog

### v1.0.0
- Initial release
- L*a*b* color space statistical transfer
- Adjustable transfer strength
- Custom visual interface with gradients
- Preset options for quick adjustments
- Batch processing support
- Comprehensive error handling

## 👨‍💻 Author

Created with ❤️ by **Lucas**

## 📄 License

This project is distributed under the MIT License. See the LICENSE file for more details.

## 🤝 Contributions

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Share your results and use cases

## 📞 Support

If you encounter any issues or have questions:
1. Check the troubleshooting section above
2. Look for similar issues in the repository
3. Create a new issue with problem details
4. Include sample images and error messages when possible

## 🌟 Acknowledgments

- Thanks to the ComfyUI community for inspiration
- Color transfer algorithm based on Reinhard et al. research
- L*a*b* color space implementation using OpenCV

---

**Transform your images with professional color grading! 🎨**

