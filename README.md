# apt-artifactory-action
Push artifacts to artifactory using this GH action

# Usage

    steps:    
      - name: Publish to artifactory
        uses: qualcomm-linux/apt-artifactory-action/upload@main
        with:
          server_url: "Artifactory url"
          target_base_repo: "Target repo"
          changes_path: ".changes file path"
          provenance_info: |
            {
              "commit": "${{ github.sha }}",
              "workflow": "https://github.com/${{ github.repository }}/actions/runs/${{ github.run_id }}"
            }
          secret: ${{ secrets.ACCESS_TOKEN }}
              


## Getting in Contact

If you have questions, suggestions, or issues related to this project, there are several ways to reach out:

* [Report an Issue on GitHub](../../issues)
* [Open a Discussion on GitHub](../../discussions)
* [E-mail us](mailto:lint.core@qti.qualcomm.com) for general questions

## License

apt-artifactory-action is licensed under the [https://spdx.org/licenses/BSD-3-Clause-Clear.html](https://spdx.org/licenses/BSD-3-Clause-Clear.html). See [https://github.com/qualcomm-linux/apt-artifactory-action/blob/main/LICENSE.txt](LICENSE.txt) for the full license text.
